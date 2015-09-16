## Hands on Spring Security

#### SpringOne2GX 2015: Wednesday 08:30AM

* The current users information is inthe Principle object.
* `@EnableWebSecuity` provides a simple login form.
* `CsrfToken`
* `WebSecurityConfigurerAdapter` is replacing the XML security configuration.
* Overide the `configure` function to provide the login page and permit all the resources(css,js).
* CSRF: Cross site request forgery.
* Spring 4.x has csrf enabled by default.
* Clickjacking. Spring security disabled iframe.
* The speaker went to walmart.com and it redirected to something else. 
  Wifi pineapple sniffs this probe request. Man in the middle attack. It is $100 device.
  The point of this demo is that we need https. 
* Content sniffing. This happens in IE. Spring security injects a header to tell IE that content sniffing is a bad idea.
  The changing the file extension from image to js will exploit in Chrome as well.
  To fight this, make sure you pass everything through security.
* Do not disable the header.
* Reflective cross site scripting. Content sensitive encoding doesnt work always. `csp().defaultSrc().self()`
* CSP is giving second layer of defense against cross site scripting. 
