---
layout: article
title: "Managing your product reviews on EchoBrain"
description: Manage your product reviews on EchoBrain - Publish reviews, edit how they are displayed, etc
image: /assets/posts/managing-your-product-reviews-on-echobrain.jpg
date: 2025-02-18
categories: ['documentation']
tags: [Documentation, Integration, Customization]
---

EchoBrain makes it easy for you to collect and display verified reviews for your product on your site. Here are some aspects of this experience that you can control within your EchoBrain dashboard


## Make your reviews visible by publishing them

Go into your EchoBrain dashboard and click on "Reviews" on the left-side bar to see all the reviews submitted for your products. Here, you will see both verified and unverified reviews.

**_Verified Reviews_**: Verified reviews are reviews that have been collected from actual purchasers of your products. These reviews have been collected by sending an email to actual buyers of your products. This email has a link for buyers to submit reviews of the products they actually bought. This email is sent to buyers about 15 days after purchase, but this number can be adjusted. To learn more about how to adjust the number of days after which EchoBrain will send review request emails to buyers, click here.

**_Unverified Reviews_**: Unverified reviews are reviews that are collected in ways other than sending an email to actual buyers of your products. For example, unverified reviews can be submitted by visitors who land on the product page itself and check the main reviews widget of that product page (the main widget has a form so that visitors can submit reviews from there). These are unverified reviews because it's not really confirmed that these reviews came from people who actually bought the product.

No reviews will be displayed on your site unless you explicitly make them visible by publishing them. You can do so by going into each review in the list of submitted reviews, and toggle the "Publish review" switch. You can also manually mark a review as verified by toggling the "Mark review as verified" switch.


![Echobrain reviews list](/assets/posts/echobrain_reviews_list.jpg)

![Echobrain reviews publish and verify](/assets/posts/echobrain_reviews_publish_verify.jpg)


## Set colors and appearance of how your reviews are displayed

Log in to your EchoBrain dashboard and click on the "Settings" link on the sidebar menu. Then, click on the "Frontend" tab and scroll down to the "Colors & appearance" section. To ease things up for you, the values for the "Primary", "Background", "Text", and "Text over Primary" colors are already pre-set according to the values you set in your Fourthwall shop theme. You can always change them if you want to use different colors for your main reviews widget. The button, input, and and image corner radius settings behave in a similar way. These are already pre-set to the settings you have in your Fourthwall shop theme so that everything aligns aesthetically when the reviews show up in your shop's product pages. There is also a "Custom syle" field where you can add custom CSS code to different HTML elements on the widget.


![Echobrain dashboard reviews frontend settings](/assets/posts/new_echobrain_dashboard_reviews_frontend_settings.jpg)

![Echobrain dashboard reviews colors and appearance](/assets/posts/echobrain_dashboard_reviews_colors_appearance.jpg)


## Set details of how your main widget is displayed

Log in to your EchoBrain dashboard and click on the "Settings" link on the sidebar menu. Then, click on the "Frontend" tab and scroll down to the "Main widget configuration" section. Here, you will be able to set values for the following:

* Max number of reviews: This is the maximum number of reviews that will be shown per page on the main reviews widget on the product page.
* Max number of images in gallery: This is the maximum number of images to be shown in the image gallery section of the main reviews widget.
* Infinite popup: If marked as "Yes", the main reviews widget will be shown as an infinite popup.
* Show section when no reviews: If marked as "Yes", the main reviews widget will be visible in all product pages regarless of whether the product has reviews or not. If marked as "No", if a product does not have reviews, it will not show the main reviews widget.
* Summary type: You can change how to show the ratings summary: just the average, just the quantity (number of reviews), or the average and the quantity.


![Echobrain reviews main widget configuration](/assets/posts/echobrain_reviews_main_widget_configuration.jpg)


## Set review request email settings

Log in to your EchoBrain dashboard and click on the "Settings" link on the sidebar menu. Then, click on the "Email" tab. Here, you will be able to set values for the following:

**Email timing:** This is the post-purchase time after which EchoBrain will send a review request email to the address associated to each order. You can have EchoBrain send these emails days, hours, or minutes after purchases happen.

**Email message content:** This is the actual content of the email requesting reviews that is sent to your supporters/customers when they buy a product you sell on your shop. You can edit things like the subject line, preview text, and the actual content of the email using some templating language.


![Echobrain review request email settings](/assets/posts/echobrain_review_request_email_settings.jpg)




<style>
.rich-text ul {
    list-style-type: disc !important;
    margin-left: 20px !important;
}
</style>
