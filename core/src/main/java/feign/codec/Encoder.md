* allows
  * object -- is encoded into -- HTTP request body
* uses
  * method parameter / has NO `@Param`
    * if some parameters are found | `feign.MethodMetadata.formParams()` -> as map is
      * -- passed to the -- `Encoder`
      * -- collected to the -- `Encoder`
* implementations
  * `GsonEncoder`
* TODO: