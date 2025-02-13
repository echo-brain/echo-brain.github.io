---
layout: article
title: "EchoBrain reviews in your Fourthwall shop: Quick Start Guide"
description: Quick Start guide to set up your EchoBrain reviews in your Fourthwall shop
image: /assets/getting-started-with-echobrain-first-steps.jpg
date: 2025-02-13
categories: ['documentation']
tags: [Documentation, Integration, Customization]
---

EchoBrain makes it simple to collect and display customer reviews on your Fourthwall shop. Follow these steps to display EchoBrain reviews into your store's design once you have completed the [EchoBrain-Fourthwall integration](https://echo-brain.com/blog/documentation/fourthwall-integration-quick-start-guide/)


## Step 1: Copy Your EchoBrain Review Code

1. Log in to your EchoBrain dashboard.
2. On the home page, locate the section labeled Code.
3. Click inside the box to select the code snippet, then copy it.


## Step 2: Access Your Fourthwall shop Theme Editor

1. Log in to your Fourthwall shop admin.
2. In the side menu, click on Site design.
3. Scroll down and select Edit code (advanced).


![Fourthwall shop admin](/assets/posts/echo-brain.com_admin_fw_dashboard_sidebar.jpg)

![Fourthwall theme editor to click on Edit code](/assets/posts/echo-brain.com_admin_fw_dashboard_edit_code.jpg)


## Step 3: Enable and Insert the Review Code

1. Check the box labeled Enable header code.
2. In the text box labeled Custom header HTML, paste the EchoBrain review code snippet you copied earlier.


![Check the Enable header code checkbox](/assets/posts/echo-brain.com_admin_enable_header_code_html.jpg)

![After inserting HTML code into textarea](/assets/posts/production-reviews-shop_admin_dashboard.jpg)


## Step 4: Showcase Your Reviews Widget
Now that you've set up your EchoBrain account and integrated it with your shop, it's time to let your customer reviews shine on your store. This step will guide you through two methods to display the EchoBrain reviews widget in your desired locations on your site.

### Method 1: Adding HTML Placeholders

To begin with, you can manually add empty HTML placeholders within your theme code. These placehodlers act as designated spots where EchoBrain will insert the reviews widget. Here's how to do it:

 **1. Identify the areas:** Identify the areas where you want the reviews widgets to appear, such as below the main product section. Add an empty HTML placeholder like the ones shown below. If you don't have access to make this code change yourself, contact support to have Fourthwall's developer team do it for you and add the placeholders in the areas that you have identified. The HTML placeholders for the currently available widgets look like the following:

*Main Reviews widget:*
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


*Ratings summary widget (to show rating average and stars):*
```liquid
<div data-reviews-summary="{ product.id }"></div>
```

 **2. Save Changes:** Save the changes to your theme code. EchoBrain's script will automatically detect these placeholders and populate them with the review widgets.

### Method 2: Using CSS Selectors

If you prefer a more dynamic approach, you can enable the "CSS selectors" feature in the EchoBrain dashboard. This allows you to specify the exact elements on your site after which the reviews widgets will be inserted. Follow these steps:

 **1. Enable CSS Selectors:** Log in to your EchoBrain dashboard and click on the "Settings" link on the sidebar menu. Then scroll down to the "Selectors" section and make sure the "Enable CSS Selectors" checkbox is checked to enable the "CSS selectors feature".

 **2. Define Selectors:** Specify the CSS selectors corresponding to the elements you want the reviews to follow. For example, if you want the widget to appear after the main product section, you might use a selector like `.product-section`, or, to be more precise, something like `.fw-section > .product-reviews > .container.wrapper > div`

 **3. Save Your Configuration:** Save your changes. EchoBrain will now insert each review widget immediately after the elements matched by your CSS selectors.


## Step 5: Save and Preview Your Changes

1. Click Save to apply the changes.
2. Go to your Fourthwall store preview to confirm the reviews are displaying correctly on your site.


### Final Steps

After applying either method, visit your store to verify that the reviews widgets are displaying correctly. If you encounter any issues, the EchoBrain support team is ready to assist you. Congratulations, you're now ready to showcase your customer reviews and build stronger trust with your audience!
By following these steps, you're ensuring that EchoBrain seamlessly integrates into your store, providing your customers with authentic and engaging reviews exactly where they're most impactful. Enjoy the enhanced engagement and credibility that EchoBrain brings to your e-commerce journey!

## Embrace the EchoBrain Advantage
Getting started with EchoBrain is more than setting up a platform; it's about laying the foundation for a more engaged, trustworthy, and customer-centric online store. By integrating EchoBrain, you're tapping into the collective power of your customer base, transforming their experiences into your brand's most compelling selling points.

Remember, every review shared through EchoBrain is a testament to your product's quality and your commitment to customer satisfaction. So, take these first steps with confidence, knowing that EchoBrain is here to support your e-commerce journey every step of the way. Welcome to the EchoBrain family, where every customer's voice contributes to your brand's ever-growing story.



