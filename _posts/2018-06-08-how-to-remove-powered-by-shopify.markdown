---
layout: post
author: Alexandru Dereveanco
title:  "How to remove “Powered by Shopify” from your e-commerce website."
date:   2018-06-08 11:37:00 +0100
background: /images/sergey-zolkin-macbook-pro.jpg
categories: ecommerce
---

As more and more Shopify merchants join our [Visely Personalized Product Recommendations][visely] app it is quite interesting to see the different patterns of how they use Shopify as a platform, the workarounds they come up with to fix a business problem and the kind of customization to their website they want.
One interesting observation I’ve made is that many Shopify store owners manage to make six figures monthly sales while still using [Free Themes][themes].
That it is pretty impressive on its own, as it proves that you can do rather well with minimum customization done to the site. But, in addition to that, merchants don’t even bother removing “Powered by Shopify” text that keeps lingering in the footer on every page.
Is this a problem? **Nope**.

It can actually be to the benefit of the website early on. Displaying “Powered by Shopify” can play the role of a [trust signal][trust-signal], but then it is better to emphasize it beyond just a lackluster link in the footer. Oh yeah, that link also helps Shopify grow its [domain authority][domain-authority] via yet another backlink to their domain.

An additional observation I’ve made in relation to the “Powered by Shopify” text during my experience helping hundreds and hundreds of [Visely Personalized Product Recommendations][visely] customers is: none of the more established stores had such a link on their website. This is quite obvious, as a brand matures and gains weight as its own recognizable entity, having “Powered by Shopify” on the site can detract from that.

That was a bit of a long introduction to saying: “You as the owner of a Shopify enabled online business, should think about removing that Shopify branding from your website at some point of your business lifespan”.

Getting a premium or a custom built theme will have the added benefit of removing the Shopify branding for you. Let’s be honest however, removing the branding is not a key factor in the decision to go with a premium or a custom theme. So let’s assume that you’ve decided to keep the free theme that served your store so well, but you also decided to remove “Powered by Shopify” text.
Great, how do you do that? Shopify has got you covered with this guide.

The guide tells you there are two options available to remove the branding: one via editing the translations by replacing “Powered by Shopify” with a single space; another by removing the liquid code which actually renders the text.

If you choose the first option the following will happen: the link to the Shopify website will be rendered with an “empty” text instead of “Powered by Shopify”. It will be invisible to the human visitors of your website, but bots will pick it up and it will still contribute to shopify.com domain authority.

If you follow the option of removing the liquid code, the link will not be rendered at all.
I believe the latter is a better option. [“Best Code is No Code”][best-no-code] is almost always true. And to be honest it is easier to adjust the liquid files than it is to tinker with the translations.

<hr />

Below are screen grabs for all ten free Shopify themes of how to remove the “Powered by Shopify ”branding text.

These all follow the same process:

1. Edit Code.
2. Find footer.liquid either in Sections or in Snippets (if you use an older, non-sectioned theme).
3. Search for “powered_by_link”.
4. Remove the code and Save.
5. Just find the free theme you are using below and watch the corresponding screen grab.

#### Supply theme
<img src="{{ '/images/supply-theme.gif' | relative_url }}" width="750" />

#### Minimal theme
<img src="{{ '/images/minimal-theme.gif' | relative_url }}" width="750" />

#### Brooklyn theme
<img src="{{ '/images/brooklyn-theme.gif' | relative_url }}" width="750" />

#### Narrative theme
<img src="{{ '/images/narative-theme.gif' | relative_url }}" width="750" />

#### Pop theme
<img src="{{ '/images/pop-theme.gif' | relative_url }}" width="750" />

#### Simple theme
<img src="{{ '/images/simple-theme.gif' | relative_url }}" width="750" />

#### Venture theme
<img src="{{ '/images/venture-theme.gif' | relative_url }}" width="750" />

#### Jumpstart theme
<img src="{{ '/images/jumpstart-theme.gif' | relative_url }}" width="750" />

#### Boundless theme 
<img src="{{ '/images/boundless-theme.gif' | relative_url }}" width="750" />

#### Debut theme
<img src="{{ '/images/debut-theme.gif' | relative_url }}" width="750" />

I hope this short guide will help understand the difference between the two options to remove the branding offered by Shopify, and it will clearly show you how to remove the code from your free Shopify theme, should you decide to do it.
<hr />

P.S.: *If you happen to be looking for a state-of-the-art product recommendations solution for you Shopify store, [take a look][visely-app-store] at our Visely Personalized Product Recommendations app in the marketplace.*

[visely]: https://visely.io
[visely-app-store]: https://apps.shopify.com/visely
[themes]: https://themes.shopify.com/themes?sort_by=most_recent&price%5B%5D=free
[trust-signal]: https://www.wordstream.com/blog/ws/2017/03/27/trust-signals
[domain-authority]: https://en.wikipedia.org/wiki/Domain_Authority
[best-no-code]: https://www.google.com/search?q=the+best+code+is+no+code
[supply-screen-grab]: /images/supply-theme.gif


