---
layout: article
title: "Forms: Adding custom forms to your shop"
description: "Building a strong connection with your customers starts with understanding their needs and preferences. One way to achieve this is through custom forms, which can collect valuable information for a tailored experience on your ecommerce site. If you’re using the EchoBrain app, this guide will walk you through creating and customizing forms to suit your business needs."
date: 2024-10-21
image: /assets/posts/echo-brain.com_admin_custom_forms_setup.jpg
categories: ['documentation']
tags: [Documentation, Customization, Forms]
---

Building a strong connection with your customers starts with understanding their needs and preferences. One way to achieve this is through custom forms, which can collect valuable information for a tailored experience on your ecommerce site. If you're using the EchoBrain app, this guide will walk you through creating and customizing forms to suit your business needs.

## Navigating to the Forms Dashboard
After logging into your EchoBrain account, you'll find yourself on the main dashboard, where you can manage various aspects of your store. To start working with forms, look to the left-side bar and click on **Forms** under the "Forms" section. This will take you to the Forms page, where you can see any existing forms and manage submissions.

![EchoBrain forms dashboard](/assets/posts/echobrain_dashboard_forms_1.jpg)

## Step-by-Step: Creating a New Form
**1. Click on "Add Form +"**: On the Forms page, you will see the option to add a new form in the upper-right corner. Click on the "Add Form +" button to create a new form. You'll be directed to a page where you can set up the details of your form.

**2. Fill Out the Form Information**: On this screen, you'll need to provide a **Name** for your form, and it's optional to include a **Description**. The description can give context for what the form will be used for, such as "Sign up for our newsletter" or "Submit your product review."

**3. Spam Protection**: You'll also notice fields for spam protection. Here you can input a list of blocked words, select an anti-spam protection level, and, if necessary, enter the secret key for the anti-spam service you choose to use. Though optional, enabling spam protection can help keep your submissions clean and relevant.

**4. Save and Get the Form Endpoint**: Once all necessary fields are filled out, click the **Save** button. A **Form Endpoint** will be generated upon saving. This endpoint is crucial, as it's where you will direct all form submissions.

![Create a new form with EchoBrain](/assets/posts/echobrain_dashboard_create_form.jpg)


## Using the Form Endpoint
Once you have your Form Endpoint, you're ready to integrate the form into your website. Here's how you can implement it using HTML or Javascript.

### HTML Form Submission
If you're using an HTML form, you'll need to set the `action` attribute of your `<form>` element to the generated Form Endpoint. For example:

```html
<form action="https://form.echo-brain.com/your-form-endpoint" method="POST" enctype="multipart/form-data">
  <input type="text" name="firstName" placeholder="First Name" required>
  <input type="text" name="lastName" placeholder="Last Name" required>
  <input type="email" name="email" placeholder="Email" required>
  <button type="submit">Submit</button>
</form>
```
In this case, the fields should always have a `name` attribute, as this is required for sending the data correctly to the Form Endpoint.

### AJAX or Fetch Submission
For a more dynamic approach, you can use JavaScript with AJAX or the Fetch API to send form data to the Form Endpoint without reloading the page. Here's a simple example using Fetch:

```javascript
const form = document.querySelector('form');
form.addEventListener('submit', async (e) => {
  e.preventDefault();

  const formData = new FormData(form);

  const response = await fetch('https://form.echo-brain.com/your-form-endpoint', {
    method: 'POST',
    body: formData
  });

  if (response.ok) {
    console.log('Form submitted successfully');
  } else {
    console.error('Error submitting form');
  }
});
```

Again, ensure that each input element in your form has a `name` attribute to ensure the data is submitted correctly.

## Managing Form Submissions
Once your forms are live, you can track and manage submissions directly within EchoBrain. Click on "Submissions" on the left-side bar, and you will get a list of all the submissions for all your active forms. You can filter the submissions to see only the ones for a specific form by using the dropdown filter on the top right corner of the list.

You can also delete submissions that are no longer relevant or flagged as spam. This gives you full control over your customer data, keeping your forms and customer interaction organized and efficient.

![Manage form submissions on EchoBrain](/assets/posts/echobrain_dashboard_form_submissions_1.jpg)

## Conclusion
Creating custom forms in EchoBrain is a straightforward yet powerful way to capture meaningful customer data. By following the steps outlined in this guide, you can seamlessly integrate forms into your ecommerce shop, whether you're collecitng newsletter sign-ups or customer feedback. Keep your audience engaged and your brand growing with EchoBrain's flexible form functionality.

Ready to create your form? Log in to EchoBrain today and start crafting a unique experience for your customers!
