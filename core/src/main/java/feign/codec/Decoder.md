* allows
  * HTTP response -- is decoded -- 1! object of given `type`
    * `type` -- correspond to the -- `feign.Target`'s `java.lang.reflect.Method.getGenericReturnType()`
* requirements to be invoked
  * `Response.status == 200` & returnType != void or `Response`
* TODO: