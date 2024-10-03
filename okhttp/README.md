OkHttp
===================

* goal
  * Feign's http requests -- are redirected to -- [OkHttp](http://square.github.io/okhttp/)
    * Reason: 🧠enables SPDY & better network control 🧠

* how to use OkHttp + Feign?
  * add OkHttp | your classpath
  * configure Feign to use the OkHttpClient

```java
GitHub github = Feign.builder()
                     .client(new OkHttpClient())
                     .target(GitHub.class, "https://api.github.com");
```
