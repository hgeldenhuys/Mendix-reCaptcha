# Mendix-reCaptcha

![](https://www.evernote.com/l/AAHIrbskkHxBpIvDqXF1NDpdxd5yKLxQ_o0B/image.png)

##Mendix version
6.5+ but if you need a version for a previous version of Mendix just pop me an email

##Introduction

The most simple, complete and flexible reCaptcha widget for Mendix.

reCAPTCHA is a free service that protects your site from spam and abuse. It uses advanced risk analysis techniques to tell humans and bots apart. With the new API, a significant number of your valid human users will pass the reCAPTCHA challenge without having to solve a CAPTCHA. reCAPTCHA comes in the form of a widget that you can easily add to your blog, forum, registration form, etc.

To use reCAPTCHA, you need to sign up for an API key pair for your site. The key pair consists of a site key and secret. The site key is used to display the widget on your site. The secret authorizes communication between your application backend and the reCAPTCHA server to verify the user's response. The secret needs to be kept safe for security purposes.

See https://developers.google.com/recaptcha/docs/start

##Typical usage scenario

Verifying a user is a human and not a droid.

##Whats included?

- The reCaptcha module containing a single java action to send your secret and response to Google.
- A reCaptcha widget 

##Configuration
After setting up your domain secret and key at Google, you will need an entity of some kind to configure your verification process since that happens server-side.

![Example entity](https://www.evernote.com/l/AAHjafifOpJHPoy1y7C5M_pD4L9qpbQj1W8B/image.png)

- Use the verfied flag to drive your Mendix app logic based on whether or not your verification passed.
- The Response Attribute is the challenge issued by the widget that will be sent along with your secret.
- The Response Attribute is the challenge issued by the widget that will be sent along with your secret.
- You could add an additional attribute for they "Key" if you don't want to use a literal string, if your site serves multiple domains

![Sample](https://www.evernote.com/l/AAEK0CHbBDhFHZc_NtFiJFXQp7tOVuJfxQEB/image.png)

![Screenshot](https://www.evernote.com/l/AAEQb-K0BD1HJbJTul2gu8NdVXSX9JG7A0MB/image.png)

##Dependencies
- None

##Properties

- **Key String**			Key string key. You need to pass wither the Key String or a Key Attribute

- **Key Attribute**		Key attribute key. You need to pass wither the Key String or a Key Attribute

- **Response Attribute**		The attribute where the response is stored for verification

- **Verfication Microflow**	The microflow that will verify with Google and must return a boolean. If false a reCaptcha.reset() will be triggered.

- **Expired Microflow**		The microflow that will trigger if the recaptcha expired. You can send back validation messages from your microflow.

- **Data Type**				The type of CAPTCHA to serve

- **Data Theme**				Widget theme

- **Data Size**				The size of the widget

- **Data Tab Index**			The tabindex of the widget and challenge. If other elements in your page use tabindex, it should be set to make user navigation easier.


##Known bugs
- None

##Frequently Asked Questions

Email and questions to [hgeldenhuys@gmail.com](mailto:hgeldenhuys@gmail.com)

