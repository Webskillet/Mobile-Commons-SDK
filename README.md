# Mobile Commons SDK

a simple php SDK for the [Mobile Commons API](https://mobilecommons.zendesk.com/hc/en-us/articles/202052534-REST-API)

Right now this has just been built for the purpose of allowing the [Webform External](https://github.com/Webskillet/webform_external) module to push data to Mobile Commons's [Profile Update](https://mobilecommons.zendesk.com/hc/en-us/articles/202052534-REST-API#ProfileUpdate) endpoint.

It has one class, MobileCommons, which is instantiated with a username, password, and (optional) subdomain - defaults to https://secure.mcommons.com

Currently, there are only two methods:

## MobileCommons->call

passed three parameters:

* __endpoint__: appended to "https://secure.mcommons.com/api/" (assuming subdomain is "https://secure.mcommons.com")
* __method__: defaults to "GET," can be set to "POST"
* __parameters__: array of parameters to send with the request (optional)

## MobileCommons->profile_update

passed an array of parameters. parameter "phone_number" is required
