# Circuit-BreakerImpl

Steps A) Add spring-boot-starter-actuator,spring-boot-starter-aop and resilience4j-spring-boot2 depedency.
      B) use @CircuitBreaker annotations on method which calling another service api.
        for eg- @CircuitBreaker(name="proxyServiceCircuitBreaker" , fallbackMethod="proxyServiceFallbackMethod")
      C) now implement fallback method, fallbackmethod name use as it is mentioend on front of fallbackMethood,
        and return type must be same as the api return type.
      D)add Exception e as parameter in fallback method
