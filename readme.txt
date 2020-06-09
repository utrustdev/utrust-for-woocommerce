=== Utrust for WooCommerce ===
Contributors: utrust
Tags: payments, payment gateway, cryptocurrencies, bitcoin, ethereum, payments, utrust
Requires at least: 5.1
Tested up to: 5.4.1
Requires PHP: 7.2
Stable tag: 1.0.0
License: MIT License (MIT)
License URI: https://github.com/utrustdev/utrust-for-woocommerce/blob/master/LICENSE

Accept Bitcoin, Ethereum, Utrust Token and other cryptocurrencies directly on your online store and get settled in fiat for 1% fee.

== Utrust for WooCommerce ==

Demo Store: [https://woocommerce.store.utrust.com/](https://woocommerce.store.utrust.com/)

==  Key Features ==

* No need to understand the world of cryptocurrencies, it’s business as usual
* Supports all crypto wallets that can scan a QR code address or input the address manually
* No volatility risk
* Prices displayed in your local currency (supports EUR, USD, GBP)
* Monthly settlements via Bank transfer (EUR, USD, GBP)
* No chargebacks
* View payments and issue refunds in Utrust Merchant Dashboard
* Since a cryptocurrency transaction does not contain any credit card or bank information, there is no need for PCI compliance

== Screenshots ==



== Requirements ==

- Utrust Merchant account
- Online store in Wordpress with WooCommerce plugin v3.0 (or greater)
- `SKU`s in all the products

== Setup ==

= On the Utrust side =

1. Go to the [Utrust Merchant dashboard](https://merchants.utrust.com).
2. [Log in](https://merchants.dev-utrust.com/sign-in), or [sign up](https://merchants.utrust.com/onboarding/sign-up) if you haven't yet.
3. In the sidebar on the left choose _Store_.
4. Click the button _Generate Credentials_.
5. You will now see your `Api Key` and `Webhook Secret`, save them somewhere safe temporarily.

   You will only be able to see the `Webhook Secret` once! After refreshing or changing page you will no longer be able to copy it. However, you can always regenerate your credentials as needed.

   WARNING: Don't share your credentials with anyone. They can use it to place and validate orders **on your behalf**.

= On the Wordpress side =

1. Go to your Wordpress admin dashboard.
2. Navigate to _WooCommerce > Settings_.
3. Choose the _Payments_ tab (or _Checkout_ in older versions).
4. Click on _Utrust_.
5. Add your `Api Key` and `Webhook Secret` and click _Save_.
6. (Optional) You can change the `Callback URL` if you are not using the default WooCommerce API.

   :warning: Make sure all your products have the `SKU` attribute, otherwise the buyer will get an error on checkout.

= Known conflicts with other Plugins =

Some plugins that may create problems with the WooCommerce API:

- [WPML](https://wpml.org/) – If configurated to use URL parameters, it redirects the HTTP requests to the WooCommerce API to the site URL with the `lang=en` parameter. One of the solutions is to change WPML to a folder system (`/en/`), another is to add the default language parameter in the `Callback URL` setting (e.g. `https://<your-site>/?lang=en&wc-api=wc_utrust`).

Found another conflict missing from this list? Please let us know [by opening an issue on GitHub](https://github.com/utrustdev/utrust-for-woocommerce/issues/new).

== Frequently Asked Questions ==

Find below a list of the most common questions about the Utrust for WooCommerce plugin.

Don't find what you're looking for in this list? Feel free to reach us [by opening an issue on GitHub](https://github.com/utrustdev/utrust-for-woocommerce/issues/new).

= Does this support both live mode and test mode for testing? =

Yes, it does - choosing between live and test mode is driven by the API keys you use. They are different in both environments. Live API keys won't work for the test environment, and vice-versa.

= What happens if I cancel the Order manually? =

We are working on it. Our API is not ready yet for merchant manual changes. If you need to change the Order status, change it in WooCommerce and then go to our Merchant Dashboard to start a refund.

== Features ==

:sparkles: These are the features already implemented and planned for the Utrust for WooCommerce plugin:

- [x] Create Order and redirect to Utrust payment widget.
- [x] Receive and handle webhook for received payment.
- [x] Receive and handle webhook for cancelled payment.
- [x] Save logs on the Wordpress admin dashboard on _WooCommerce > Status > Logs_.
- [x] Support pre-orders paid upfront (it doesn't support charge on release date).
- [ ] Sends HTTP request to the Utrust Merchant API when an Order status is updated manually.
- [ ] Errors handling class to improve errors logs.
- [ ] Compatibility with WooCommerce earlier than 3.0.

== Support ==

Feel free to reach [by opening an issue on GitHub](https://github.com/utrustdev/utrust-for-woocommerce/issues/new) if you need any help with the Utrust for WooCommerce plugin.

If you're having specific problems with your account, then please contact support@utrust.com.

In both cases, our team will be happy to help.

== Contribute ==

You can contribute by simply letting us know your suggestions or any problems that you find [by opening an issue on GitHub](https://github.com/utrustdev/utrust-for-woocommerce/issues/new).

You can also fork the repository on GitHub and open a pull request for the `master` branch with your missing features and/or bug fixes.
Please make sure the new code follows the same style and conventions as already written code.
Our team is eager to welcome new contributors into the mix.

== Changelog ==

= 1.0.1 =

* Update compatibility to WooCommerce 4.1.1
* Add readme.txt

= 1.0.0 =

* Release of stable version

== License ==

The Utrust for WooCommerce plugin is maintained by the Utrust development team, and is available to the public under the GNU GPLv3 license. Please see [LICENSE](https://github.com/utrustdev/utrust-for-woocommerce/blob/master/LICENSE) for further details.

&copy; Utrust 2020