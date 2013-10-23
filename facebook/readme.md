# Login with Facebook

- partial.js version +v1.2.7-0
- copy **facebook.js** to __/your-partialjs-website/modules/__
- [EXAMPLE](https://github.com/petersirka/partial.js-modules/tree/master/facebook/example)

## Functions and Events

```javascript

var facebook = controller.module('facebook');

/*
	Get URL to login
	@key {String} :: facebook key
	@url {String} :: redirect after Facebook authorization
	return {String}
*/
facebook.redirect(key, url);

// EXAMPLE: controller.redirect('key', controller.host('/login/facebook/'));


/*
	Get URL to login
	@key {String} :: facebook key
	@secret {String} :: facebook secret
	@code {String} :: code parameter (from URL address - Facebook return this parameter)
	@url {String} :: redirect after Facebook authorization
	@callback {Function} :: function(err, user) {}
	return {String}
*/
facebook.profile(key, secret, code, url, callback);

// EXAMPLE: controller.redirect('key', 'secret', controller.get.code, controller.host('/login/facebook/'), function(err, user) {});
```