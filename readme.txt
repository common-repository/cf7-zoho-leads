=== Contact Form 7: Zoho Leads integration ===
Contributors: jcornutt
Donate link: https://joscor.com/cf7-zoho-leads
Tags: cf7, contact form 7, zoho, crm, zoho crm, zoho leads, zoho api, leads, smb, contact form, cf7 integration, wordpress, curl, xml
Requires at least: 3.2
Tested up to: 4.7.2
Stable tag: 4.7
License: GPLv2
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Zoho Leads integration for Contact Form 7 forms.


== Description ==

The Zoho Leads integration for Contact Form 7 plugin allows existing CF7 users to
automatically create Zoho Leads entries on form submission. When a user
enters their information into a CF7 form and hits submit, this plugin will
forward their information to Zoho Leads as well as let CF7 continue its
form submission process. Note - This plugin is developed, maintained, and
supported by an independent developer. The developer has no affiliation with
Contact Form 7 or Zoho.

= Zoho Leads integration =

This plugin interacts with the third-party Zoho CRM API (Application Programming Interface)
in order to create new Leads. This is a public web service provided by Zoho and
additional information can be found [here](https://www.zoho.com/crm/help/api/).


== Features ==

* Easy CF7 to Zoho Leads field mapping
* Convenient, intuitive shortcode
* Lead Source is the title of the CF7 form
* Seamless integration and no change to contact form flow

== Installation ==

1. Download the plugin and unzip to your wp-content/plugins directory
2. Alternatively, just upload the zip file via the WordPress plugins UI
3. Activate plugin via Wordpress admin
4. Include the following shortcode on your page or post

= Shortcode usage =

`
[cf7lead cf7_id="[CF7_Form_ID]"]
`

Replace *[CF7_Form_ID]* with the ID of your CF7 form.

If you're having issues with the plugin, please set the
shortcode "debug" option to "true". This will allow
the plugin to show debug / error messages to the page (do not
use on production systems as the messages will be public).

`
[cf7lead cf7_id="[CF7_Form_ID]" debug="true"]
`

= CF7 to Zoho Leads mapping =

By default, the current field mapping looks like this -

* *CF7 -> Zoho Leads*
* company -> Company
* first-name -> First Name
* last-name -> Last Name
* email -> Email
* phone -> Phone
* title -> Title

For a list of Zoho Leads fields, please check out the [Zoho Leads docs](https://www.zoho.com/crm/help/api/insertrecords.html#Insert_records_into_Zoho_CRM_from_third-party_applications) for more info.

To change the field name mapping, use the shortcode's "fields" attribute.
This is a '|' (pipe) separated list of '=' (equal) separated strings.
For instance, *fields="Company=company|First Name=first-name|Last Name="* is a
valid fields string to use. It says to map the Zoho Leads field "Company"
to the CF7 field "company" (everything here is case sensitive), the Zoho Leads
field "First Name" to "first-name", and to not map "Last Name" to anything
(which means that the Zoho Lead field "Last Name" will have no value).


== Changelog ==

= 0.0.4 =
* Fix for null-checking on PHP v5.5 and older
* Updated settings table styles

= 0.0.2 =
* Fix README shortcode name

= 0.0.1 =
* Genesis
