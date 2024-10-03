Jackson Codec
===================

* goal
  * via Jackson
    * encode JSON
    * decode JSON


```java
GitHub github = Feign.builder()
                     .encoder(new JacksonEncoder())
                     .decoder(new JacksonDecoder())
                     .target(GitHub.class, "https://api.github.com");
```

*  `ObjectMapper` / provided | `JacksonEncoder` & `JacksonDecoder` -- can be -- customized

```java
// customize the ObjectMapper 
ObjectMapper mapper = new ObjectMapper()
        .setSerializationInclusion(JsonInclude.Include.NON_NULL)
        .configure(SerializationFeature.INDENT_OUTPUT, true)
        .configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);

GitHub github = Feign.builder()
                     .encoder(new JacksonEncoder(mapper))
                     .decoder(new JacksonDecoder(mapper))
                     .target(GitHub.class, "https://api.github.com");
```
