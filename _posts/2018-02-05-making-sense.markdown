---
layout: post
author: Alexandru Dereveanco
title:  "Making sense of Product Recommendation Widgets"
date:   2018-02-05 11:37:00 +0100
background: /images/making-sense/retail-store.jpg
categories: ecommerce
---
Hey folks, it’s Alex here again, co-founder of nemo.ai, the team behind [Visely Product Recommendations][visely].

In the first part of this four-part series [I’ve laid out][setup-recommendations] simple guidelines for an efficient product recommendations setup for an e-commerce online store.

Here, I’ll dive deeper into various product recommendations widgets, what exactly these are and how they work.

To start, let’s group the widgets together as it makes understanding them a bit easier.

We end up with the following categories of product recommendations widgets:

* Widgets based on non product related attributes
* Widgets based on product content and attributes
* Widgets based on collaborative behaviour in relation to a product
* Widgets based on individual user behaviour in relation to a product


Let's analyze them all.

#### Recommendations Based on Non Product Related attributes.

<img src="{{ '/images/making-sense/most-popular.png' | relative_url }}" class="inline-image" />

##### Most Popular / Best Sellers

One of the most frequently used widgets, *Most Popular* is based on ordering products within the store’s catalog or its subset by the number of times the products were purchased by the entire user base within a predefined, usually quite long, time frame. The time frame varies from 3 months to the entire lifespan of the store.

If the time frame used is a few months long, the *Most Popular* widget can adapt itself to the seasonality of the customers purchasing habits, and can evolve to better display the changing trends of shopping based on the season.


Another aspect of the widget is the different level of importance given to more recent purchases when compared to older ones. Depending on this, *Most Popular* recommendations widget can play the role of an overview of historical popularity of products or an overview of trends in purchase popularity of products.

Business importance of this widget is quite obvious. As a e-commerce entrepreneur you want to give your shoppers a clear view of your best selling items, as [Pareto Principle][pareto] also works for sales of products online. Our statistics show that roughly 27% of the products will bring 74% of the revenue.

##### Trending Now

<img src="{{ '/images/making-sense/trending-now.png' | relative_url }}" class="inline-image" />

*Trending Now* product recommendations widget showcases products which are currently viewed by store’s visitors as a group.

Order of these products is determined by the number of views of a product within a time frame. When compared to the time frame used for *Most Popular* widget, the *Trending Now* time frame is usually shorter. It can vary from several days to several weeks.

Product view is a much more frequent event, compared to a purchase event, making *Trending Now* a more dynamic widget when compared with *Most Popular*. It shows a level of browsing popularity of products in store’s catalog.

##### New Arrivals

*New arrivals* product recommendations widget displays products recently added to the store’s catalog.

The order of the products is determined by the dates these products where published on the store, newest first.

Depending of the intent of the widget, a limited time frame could be used. This time frame characterises the products that fit the ruleset as “New”.

Alternatively, if the intent of the widget is “Newest Products”, the time frame can be expanded indefinitely into the past, and all of the products from the catalogue or from the subset of the catalogue will be sorted, newest first.

Showcasing new products is especially useful in case your store has a significant percentage of returning visitors and customers, as these users are likely more interested in the new additions to your store.

#### Recommendations Based on Product Content and Attributes
##### Similar Products

*Similar Products* recommendations widget showcases products that have the highest degree of similarity between them, based on the entire set of the attributes products have. Both linguistic, relational and more recently, visual content is used to determine the degree of similarity. The key here is that all of the attributes are used to determine similarity.

It needs to be said that every recommendation system has its own ruleset when it comes to determining similarity.

##### Related products
*Related products* widget is semantically quite close to the *Similar Products* widget, the difference between the two is that products showcased in *Related Products* widget are similar to each other on a limited subset of properties.

For example: *More in this Collection* displays products that are related via the collection they are in, but can differ substantially in other attributes. Another example would be *Products in Same Colour*, which will showcase products that have the same value for the colour attribute as the origin product.

#### Recommendations Based on Collaborative Behaviour in Relation to a Product
##### Customers who bought this also bought
This widget displays products which are logically linked with the “context” product by being in a customer purchase history.

This is best clarified with an example: let’s say a customer buys product A and then later buys product B. This type of recommendation widget will show product A as recommendation for product B and vice versa.

Customers purchasing these products create logical relationships between them, and when the same approach is applied to the entire customer base and purchase history of the store, relevant relationships are built for the products.

##### Customers who bought this also viewed
This widget is similar to the previous one but varies in action performed on product A. Instead of buying product A, the action is viewing product A. So the example becomes: “A customer views product A and then later buys product B”. This type of recommendation widget will show product B as recommendation for product A.

##### Frequently bought together

While this product recommendation widget may seem to be same with *Customers who bought this also bought* initially, logically it is quite different.

This product recommendations widget presents products that were bought together in the same order. The widget increases average order value by recommending complementary products, like “a tie” for “a shirt” or “a phone case” for “a phone”, etc.

Edge cases are disregarded when the entire purchase history for an active store is considered.

This type of widgets work best on high intent pages or actions, like “Cart Page” or on add to cart action.

#### Recommendations Based on Individual User Behaviour in Relation to a Product
##### Recently Viewed

<img src="{{ '/images/making-sense/recently-viewed.png' | relative_url }}" class="inline-image" />

*Recently Viewed* is one of the simplest personalised widgets as it contains the product navigation history for an individual user and its content is personalised for that particular user. This widget is useful as a reminder to complete an abandoned interaction with a product.

#### Visely Specifics and Implementation Decisions.
<img src="{{ '/images/making-sense/ymal.png' | relative_url }}" class="inline-image" />

In our implementation of [Visely Product Recommendations][visely], we’ve decided to combine product content and collaborative behaviour recommendations into one, over-arching product recommendation widget — *You May Also Like*.

We recognise that product details page real estate is extremely valuable and cluttering the page with multiple widgets with a single logical relation will detract from the shoppers experience and result in lower conversions.

Statistics show that only 17% of visitors to the product details page scroll [below the fold][fold].

Additionally this combined approach gives the *You May Also Like* widget discrete, intent based, customer generated click through data to learn and adapt itself to maximise conversion.

That’s it! I hope this quick article has clarified a few aspects of product recommendations for you.

<hr />

*In the [next instalment][purchase-attribution] we’ll talk about sale attribution in the context of product recommendations systems. Stay tuned.*

*P.S.: If you happen to be a Shopify store owner, [take a look][visely-app-store] at our Visely Product Recommendations app in the marketplace.*

[visely]: http://visely.io
[visely-app-store]: https://apps.shopify.com/visely
[setup-recommendations]: {{ site.baseurl }}{% post_url 2018-01-22-setup-product-recommedations %}
[pareto]: https://en.wikipedia.org/wiki/Pareto_principle
[fold]: https://en.wikipedia.org/wiki/Above_the_fold
[purchase-attribution]: {{ site.baseurl }}{% post_url 2018-02-19-purchase-attribution %}

