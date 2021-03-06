=== Paid Memberships Pro - VAT Tax Add On ===
Contributors: strangerstudios
Tags: paid memberships pro, pmpro, tax, vat, eu
Requires at least: 3.5
Tested up to: 4.7.3
Stable tag: .4.1

Calculate VAT tax at checkout and allow customers with a VAT Number to avoid the tax.

== Description ==

This plugin adds a new section on the Membership Checkout form titled "European Union Residents VAT". The customer can select their EU country of residence from a drop-down box or enter their VAT number to avoid the tax. The entered VAT number is validated using the SOAP service provided through the European Commission (http://ec.europa.eu/taxation_customs/vies/technicalInformation.html).

VAT rates are automatically calculated based on the constant rates defined in the plugin. The rates in our plugin are those currently listed by the European Commission (http://ec.europa.eu/taxation_customs/index_en.htm)

== Installation ==

1. Make sure you have the Paid Memberships Pro plugin installed and activated.
1. Upload the `pmpro-vat-tax` directory to the `/wp-content/plugins/` directory of your site.
1. Activate the plugin through the `Plugins` menu in WordPress.
1. Update your payment settings to make sure you are collecting billing address at checkout.
1. If you are using a gateway like PayPal Express that doesn't collect a billing address, install and activate the Add Address for Free Levels addon.

== Frequently Asked Questions ==

= I found a bug in the plugin. =

Please post it in the GitHub issue tracker here: https://github.com/strangerstudios/pmpro-vat-tax/issues

For immediate help, also post to our premium support site at http://www.paidmembershipspro.com for more documentation and our support forums.

= I need help installing, configuring, or customizing the plugin. =

Please visit our premium support site at http://www.paidmembershipspro.com for more documentation and our support forums.

== Changelog ==

= .4.1 =
* BUG: Changed GB back to UK in countries list.

= .4 =
* BUG: Fixed bug where checkouts to non-EU countries with the EU Country value not set were failing. These checkouts should go through fine without VAT applied.
* BUG/ENHANCEMENT: Hiding VAT stuff from free levels and not requiring an EU country.
* ENHANCEMENT: Now saving the VAT Number, VAT Country, and VAT Tax Rate to the order notes.
* ENHANCEMENT: Also added VAT Number, VAT Country, and VAT Tax Rate to the orders export CSV.
* ENHANCEMENT: Also added VAT Number, VAT Country, and VAT Tax Rate to the invoice bullets.
* ENHANCEMENT: Added pmprovat_getTaxRate($country, $state = NULL) function to get tax rates out of our global array.
* ENHANCEMENT: Can choose a "Seller Country" from the payment settings page. In the future, we may disallow customers from the same member country as the vendor from using their VAT Number for exemption. However, we need to verify the legal details of that first. For now, the seller country is just stored in the DB as an option.
* ENHANCEMENT: Better wrapping of strings for localization.

= .3 =
* FEATURE: Now supports PayPal Express and TwoCheckout
* BUG: Fixed various issues with the hide/show logic for the VAT area at checkout.
* BUG: Fixed various issues with VAT Number validation
* BUG: Change UK to GB in the country list.
* BUG: If Greece was selected, it sent VAT prefix as "GR" while it should be "EL".
* ENHANCEMENT: Added Croatia (HR) to the country list.
* ENHANCEMENT: Ordered the country list by the country name.
* ENHANCEMENT: Up to date VAT rates.

= .2 =
* BUG: Fixed bug where VAT was not applied if only a country of residence was chosen vs having the billing country set.
* ENHANCEMENT: Now setting the country of residence to the billing address if the country of residence is blank when the billing address is changed.

= .1.1 =
* BUG: Fixed warnings and issues when $bcountry was not available.

= .1 =
* Original version.
