---
layout: post
author: Alexandru Dereveanco
title:  "How to Setup Product Recommendations"
subtitle: "Learn how to setup product recommendations on an ecommerce website"
date:   2018-01-22 11:37:00 +0100
background: /images/setup-product-recommendations/support.jpg
categories: ecommerce
---

Hi everyone, I’m Alex, co-founder at nemo.ai, the team behind [Visely Product Recommendations][visely].

Some time ago we launched our brand new recommendation engine and integrated it with [Shopify][visely-app-store], which is an excellent e-commerce platform with a bustling app marketplace.
Our CEO, Sergiu Ciumac, has [done an excellent write-up][startup] on how we started our company.

So the dust has settled, customers have signed up and data has started to flow. It is time for us to share with the community some insights we’ve learned so far from real-world use cases of our product recommendation system.
In a series of articles, I’ll address several topics which we believe will be helpful for up and coming e-commerce entrepreneurs.

I’ll start with a four-part article talking about how to setup product recommendations widgets to maximise conversion. I’ll also [dive deeper][making-sense] into product recommendation widgets. [I’ll explain][purchase-attribution] how a recommendation system attributes a purchase and [I’ll lay out][personalized-shopping] a simple framework of rules to help decide if your online store needs personalisation.

#### Observations
While helping our customers achieve the best possible results for their store’s conversion, we’ve observed that a lot of store owners have their own preferences when it comes to deciding which recommendation widgets to use on which pages.

Such flexibility, is of course, great, but can result in setups that are not efficient, with sub-par conversion performance.

In order to help shop owners, we’ve decided to share a set of simple guidelines for an efficient and converting product recommendations setup.

#### Funnel & Context

Here it is best to take note of the following three concepts: browse/checkout funnel, page context and product recommendations widget context.

##### Browse/Checkout Funnel

Every store and its online shopping experience can be modelled by a funnel, with the landing pages are on top and checkout and purchase on the bottom.

<img src="{{ '/images/setup-product-recommendations/checkout-funnel.png' | relative_url }}" class="inline-image" />

The vast majority of times the visitors to your online store will just browse the site to familiarise themselves with it and the catalogue it offers. The majority of times these sessions will not result in purchased products. This means that they usually stay on top of the funnel.

It is your goal as the e-commerce entrepreneur to design and build your online store to encourage your visitors to go further down this funnel, and ultimately make the purchase.

This is one of the purposes of product recommendations widgets - drive your visitors lower into Browse/Checkout funnel.

##### Page Context
This one is quite simple to figure out, just answer the question: *“What does the page talk about?”*
This is best illustrated with a few examples:

The *Homepage* usually talks about the entire store, its various aspects and perhaps the current ongoing promotions, sales etc.

A *Collection* page often lists the products within it but also have informational content about it.

A *Product Details* page quite obviously describes a very specific product.

*Content Pages* are trickier because their context varies from general purpose information to brand-related information to product information.

For a content page that describes the approach of a store to taking suits measurements the answer to the question is “Suits”, which often times is a collection within that store. So in this example context is “Suits” collection.

In another example, if a Content page contains a size guide, the answer to the question is “Store” as it contains store specific information, so its context is “Store”.

<img src="{{ '/images/setup-product-recommendations/page-context.png' | relative_url }}" width="700" />

##### Product Recommendation Widget Context
Similarly to a page on the site, a product recommendation widget has its own context.

For *Most Popular / Best Sellers*, *Trending Now* and *New Arrivals* context is the store.

For *Most Popular in Collection*, *Trending Now* in *Collection* and *New Arrivals in Collection* widgets context is a collection.

For *You May Also Like*, *Also Bought*, *Similar Products* and *Related Products* widget context is a product.

<img src="{{ '/images/setup-product-recommendations/widget-context.png' | relative_url }}" width="700" />

You can probably already see how store pages relate to product recommendations widgets via the respective context.

The thought process is quite simple:
1. Answer these two questions: “Where in the browse/checkout funnel is the page?” and “What does the page talk about?”
2. If the page is up in the funnel and its context is the entire Store, use Most Popular, Trending Now or New Arrivals widgets.
3. If the page’s context is something other than the entire store, use widgets that match via the page’s context.

#### Example
To end this short write-up, we’d like to offer you an example product recommendation setup for one of our customers :

1. *Most Popular* widget on Home Page
2. *Trending Now* on Collection Pages.
3. *You May Also Like* on Product Details Pages.

Using this setup, product recommendations consistently achieve remarkable performance stats for the store:

1. 18.55% of the total online revenue is driven by product recommendations.
2. The product recommendations conversion rate is 2.48%, compared to the regular, non-recommendations conversion rate of 0.98%.

Of course, this is just one way to tackle product recommendations and while these guidelines are helpful, you should also pay great attention to where exactly product recommendations are shown on the page.

In addition, personalised recommendations don’t necessarily follow the same line of thought, but the approach laid out here can serve as a start and will help you build your product recommendations setup more efficiently and achieve higher conversion!

<hr />

*In the [next instalment][making-sense] of this series, I’ll dive deeper into various recommendations widgets. Stay tuned.*

*P.S.: If you happen to be a Shopify store owner, [take a look][visely-app-store] at our Visely Product Recommendations app in the marketplace.*

[visely]: http://visely.io
[visely-app-store]: https://apps.shopify.com/visely
[startup]: https://medium.com/@addictedcs/how-we-bootstrapped-a-startup-ea7142933a87
[making-sense]: {{ site.baseurl }}{% post_url 2018-02-05-making-sense %}
[purchase-attribution]: {{ site.baseurl }}{% post_url 2018-02-19-purchase-attribution %}
[personalized-shopping]: {{ site.baseurl }}{% post_url 2018-05-03-personalized-shopping-experience %}

