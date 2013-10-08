ChildBrowserAuth
================


An extension of the ChildBrowser plugin to allow access to password-protected resources.

The username and password must be represented as a Base&4 encoded parameter and passed to the openWebPage function of ChildBrowser as
the second parameter:

							window.plugins.childBrowser.showWebPage(url, authToken);
							

To construct a basic auth token from a user name and password, simply use this function:

make_base_auth: function (user, password) {
		var tok = user + ':' + password;
		var hash = window.btoa(tok);
		return "Basic " + hash;
}
							


