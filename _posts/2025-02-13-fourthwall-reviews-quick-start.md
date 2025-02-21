---
layout: article
title: "EchoBrain reviews in your Fourthwall shop: Quick Start Guide"
description: Quick Start guide to set up your EchoBrain reviews in your Fourthwall shop
image: /assets/posts/echobrain-reviews-in-your-fourthwall-shop-quick-start-guide.jpg
date: 2025-02-13
categories: ['documentation']
tags: [Documentation, Integration, Customization]
---

EchoBrain makes it simple to collect and display customer reviews on your Fourthwall shop. Follow these steps to display EchoBrain reviews into your store's design once you have completed the [EchoBrain-Fourthwall integration](https://echo-brain.com/blog/documentation/fourthwall-integration-quick-start-guide/)


## Step 1: Copy Your EchoBrain integration code snippet

1. Log in to your EchoBrain dashboard.
2. On the home page, locate the section labeled Code.
3. Click inside the box to select the code snippet, then copy it.


![Echobrain dashboard code](/assets/posts/new_echobrain_dashboard_code.jpg)


## Step 2: Access Your Fourthwall shop Theme Editor

1. Log in to your Fourthwall shop admin.
2. In the side menu, click on Site design.
3. Select the "Style" option on the upper left part of the Theme Editor.
4. Scroll down and select Edit code (advanced).


![Echobrain access Fourthwall theme editor](/assets/posts/echobrain_access_fourthwall_theme_editor.jpg)


## Step 3: Enable and Insert the Review Code

1. Check the box labeled Enable header code.
2. In the text box labeled Custom header HTML, paste the EchoBrain review code snippet you copied earlier.


![Echobrain Enable and Insert review snippet](/assets/posts/echobrain_enable_and_insert_review_snippet.jpg)


## Step 4: Showcase Your Reviews Widget
Now that you've set up your EchoBrain account and integrated it with your shop, it's time to let your customer reviews shine on your store. This step will guide you through two methods to display the EchoBrain reviews widget in your desired locations on your site.

### Method 1: Adding HTML Placeholders

To begin with, you can manually add empty HTML placeholders within your theme code. These placehodlers act as designated spots where EchoBrain will insert the reviews widget. Here's how to do it:

 **1. Identify the areas:** Identify the areas where you want the reviews widgets to appear, such as below the main product section. Add an empty HTML placeholder like the ones shown below. If you don't have access to make this code change yourself, contact support to have Fourthwall's developer team do it for you and add the placeholders in the areas that you have identified. The HTML placeholders for the currently available widgets look like the following:

##### *Main Reviews widget:*
 ```liquid
 <div data-reviews="container">
    <script type="application/json" data-reviews="json">
        {
          "product_id": "{ product.id }",
          "product_title": "{ product.title }",
          "product_image": "{ product.images[0].src | img_url: '720x' }",
          "product_url": "{ product.url }"
        }
    </script>
</div>
```

 One of the most important things when you add the above code is for you to include the `data-reviews="container"` attribute.


##### *Ratings summary widget (to show rating average and stars):*
```liquid
<div data-reviews-summary="{ product.id }"></div>
```

 **2. Save Changes:** Save the changes to your theme code. EchoBrain's script will automatically detect these placeholders and populate them with the review widgets.

### Method 2: Using CSS Selectors (No Code, Recommended)

If you prefer a more dynamic approach, you can enable the "CSS selectors" feature in the EchoBrain dashboard. This allows you to specify the exact elements on your site after which the reviews widgets will be inserted. Follow these steps:

 **1. Enable CSS Selectors:** Log in to your EchoBrain dashboard and click on the "Settings" link on the sidebar menu. Then, click on the "Frontend" tab and scroll down to the "Selectors" section and make sure the "Enable CSS Selectors" checkbox is checked to enable the "CSS selectors feature".


![Echobrain dashboard reviews frontend settings](/assets/posts/new_echobrain_dashboard_reviews_frontend_settings.jpg)

![Echobrain dashboard css selectors settings](/assets/posts/new_echobrain_dashboard_css_selectors_settings.jpg)


 **2. Define Selectors:** Specify the CSS selectors corresponding to the elements you want the reviews to follow.
 For each widget, you have the option to define a CSS selector, and a CSS wrapper.
 
 The CSS selector is the HTML element after which you want the review widget to be placed. For example, if you want the main widget to show up after the main product section, you might use a selector like `.product-section`, or, to be more precise, something like `.fw-section > .product-section`

 The CSS wrapper is the HTML class structure, made of div elements, that you want the widget to have. For example, you may want the main widget to be wrapped by a HTML structure made of 3 div elements with the classes ".fw-section", ".product-reviews", and ".container.wrapper", and 1 div element without a class. In this case, the CSS wrapper would be `.fw-section > .product-reviews > .container.wrapper > div`, and the HTML structure of the widget would look like this:

```HTML
 <div class="fw-section">
    <div class="product-reviews">
       <div class="container wrapper">
          <div>
             <!-- Reviews widget will start here -->

             <!-- Reviews widget will end here
          </div>
       </div>
    </div>
</div>
```

 **3. Save Your Configuration:** Save your changes by clicking the "Save" button. EchoBrain will now insert each review widget immediately after the elements matched by your CSS selectors.


## Step 5: Repeat Step 4 for the different review widgets you want to display

In EchoBrain, so far, we offer 2 review widgets to display on your product page: the main reviews widget, and the ratings summary widget.

##### *Main Reviews widget:*

This is the main widget that is intended to show up in each of your product pages, showcasing the reviews of each your products. It will show a summary of your product star rating, and it will also show details of each review that was published by your team. [Click here](https://echo-brain.com/blog/documentation/managing-your-reviews/) to learn more about managing your shop's reviews.

![Beautiful Bastard products plush throw blanket EchoBrain](/assets/posts/beautifulbastard_products_plush-throw-blanket-echobrain.jpg)

##### *Ratings Summary widget:*

This is the widget that shows a summary of the star rating of your product. It is calculated by averaging all the published reviews of your product. Many creators and sellers choose to show this widget below the product title on the product page or somewhere on each tile on a collection page:

![EchoBrain reviews rating summary widget](/assets/posts/echobrain_reviews_summary_widget.jpg)

### Final Steps

After applying either method, visit your store to verify that the reviews widgets are displaying correctly. If you encounter any issues, the EchoBrain support team is ready to assist you. Congratulations, you're now ready to showcase your customer reviews and build stronger trust with your audience!
By following these steps, you're ensuring that EchoBrain seamlessly integrates into your store, providing your customers with authentic and engaging reviews exactly where they're most impactful. Enjoy the enhanced engagement and credibility that EchoBrain brings to your e-commerce journey!


### Next Steps
- [Click here](https://echo-brain.com/blog/documentation/managing-your-reviews/) to learn how to manage the way reviews are displayed/requested on your shop: Edit number of days post-purchase to send review request emails, choose where on your pages to show your reviews, how reviews are displayed, etc.
- [Click here](https://echo-brain.com/blog/documentation/managing-your-reviews/#make-your-reviews-visible-by-publishing-them) to learn how to check the reviews that have been submitted by your customers, reply to them, and publish the ones you want to showcase in your product pages.
- [Click here](https://echo-brain.com/blog/documentation/exporting-and-importing-reviews-with-echobrain/) to learn how to export/import reviews in EchoBrain.


<style>
.rich-text ul {
    list-style-type: disc !important;
    margin-left: 20px !important;
}
</style>
