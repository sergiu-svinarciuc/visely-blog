---
layout: post
author: Alexandru Dereveanco
title:  "Purchase Attribution in Product Recommendations"
date:   2018-02-19 11:37:00 +0100
background: /images/purchase-attribution/credit-card.jpg
categories: ecommerce
---
I’m continuing with the series of write up on various aspects of product recommendation systems. Previously [I’ve laid out][setup-recommendations] simple guidelines for an efficient product recommendations setup on an online e-commerce store, and [I’ve also explained][making-sense] the purpose of various recommendation widgets.

To continue the quick foray into product recommendations, let’s take a look at how a recommendation system decides if a purchase made on the site can be attributed to it.

#### Purchase Attribution
What is purchase attribution?

*Purchase attribution is a set of rules which determine whether to credit a purchase event to product recommendations functionality.*

All purchase attribution rules have at their centre several events that are triggered by the visitors in regards to the product recommendations and the online store itself. These events are clicks on recommendations widgets, additions to cart and purchases. There is also the concept of attribution window.

##### Click Event
This is a simple click of one of the products presented to the shopper by the product recommendations system. The broader term is “touch point” as recommendations can be offered outside of the web related context, but for the purpose of this write-up, the click is enough.

##### Addition to Cart Event
This happens when a shopper adds an item to the cart.

##### Purchase Event
This event happens when a shopper actually purchases an item from the online store.

##### Attribution Window
This is a predefined period of time during which product recommendation events and subsequent purchases can be claimed to be related. Depending on the implementation of the purchase attribution rules, there can be multiple attribution windows.

#### Purchase Attribution Methods
The two most commonly used purchase attribution rulesets are direct click to purchase attribution and click to purchase attribution with an intermediary add to cart event. Let’s take a look at both of them.

##### Direct Click to Purchase Attribution
In this type of attribution ruleset, the two key events are click and purchase.

An example of the simplest click to purchase attribution ruleset would be:

1. Is there a purchase of the product event?

2. Was there a product recommendation click for the purchased product by the same user within the period defined as attribution window before the purchase event?

3. If the answer to both questions is yes, then the purchase can be attributed to product recommendation service.

 <img src="{{ '/images/purchase-attribution/attribution.png' | relative_url }}" class="inline-image" />

In the above example the teal and purple bars along the timeline represent the duration of click to purchase attribution windows and in the case of the interaction with product A (teal) the purchase would be attributed to product recommendation service, and Product B (purple) will not.

A more complicated purchase attribution ruleset would take into account if the product recommendation click was the first, the last or the only touch point with the product in users path to purchase, of course, within the attribution window.

It’s worth mentioning that attribution window can vary from 6 hours to 30 days and beyond, and is very specific to the recommendation service. It also can be dynamic, based on various properties of the catalogue that product recommendation service uses.

Also, the following general rule is true: the shorter the attribution window the stronger the relationship between events is. It is easier to argue that two events have a stronger relationship between them if they have occurred close in time to each other.

Having said this, there is a natural tendency to have a direct, linear dependency between the average price of the products within a catalogue and the duration of the attribution window. The more expensive the products in the catalogue, the longer the attribution window tends to be, as the purchase of more expensive products is a longer process when compared to cheap products, and a click event that happened a long time ago can lead to a purchase. This happens because customers occasionally use carts as impromptu wish lists.

##### Click to Purchase Attribution via Add To Cart

An alternative to the direct click to purchase ruleset is an attribution ruleset that uses the “Add to Cart” event an intermediary, but none the less, very important step.

With this approach, the attribution window now governs the time interval between the click and add to cart events on the site. The duration of this attribution window is usually short, from one to several hours. And the general rule described above is also true here: the shorter this duration is, the stronger the connection between product recommendation click and add to cart is.

An example of click to purchase through add to cart ruleset would be following, and it has two steps:

Step 1:

1. Is there an add product to cart event?
2. Was there a product recommendation click for the product added to cart by the same user within the period defined as attribution window before the add to cart event?
3. If the answer to both questions is yes, then add to the cart can be attributed to product recommendation service.

Step 2:

1. Is there a purchase product event?
2. Was there an add to cart event by the same user, for the purchased product attributed to the product recommendation service?
3. If the answer to both questions is yes, then add to the cart can be attributed to product recommendation service.

 <img src="{{ '/images/purchase-attribution/attribution-2.png' | relative_url }}" class="inline-image" />

With this type of ruleset, the time elapsed between add to cart and purchase is secondary, so it doesn’t really matter when the purchase is actually made, as the logical link to the product recommendation service has been established via the add to the cart event.

The previous ruleset, direct click to purchase attribution, solves the cart as “wish list” problem by extending the attribution window duration, and thus the relationship between events becomes compromised. The approach with an intermediary “add to cart” step solves this problem without compromising the relationship between events.

Both of these approaches rely on a predefined sequence of events and are prone to various edge case scenarios. There are several data reconciliation approaches that help with these but are out of the scope for this write-up.

Hopefully, this brings a bit of clarity for you on how a product recommendation system considers purchases its own.


*[In the next article][personalized-recommendations] in this series, I’ll talk about a framework to use when deciding if your store needs personalised recommendations. Stay tuned.*

*P.S.: If you happen to be a Shopify store owner, [take a look][visely-app-store] at our Visely Product Recommendations app in the marketplace.*

[visely]: http://visely.io
[visely-app-store]: https://apps.shopify.com/visely
[making-sense]: {{ site.baseurl }}{% post_url 2018-02-05-making-sense %}
[setup-recommendations]: {{ site.baseurl }}{% post_url 2018-01-22-setup-product-recommedations %}
[personalized-recommendations]: {{ site.baseurl }}{% post_url 2018-05-03-personalized-shopping-experience %}


