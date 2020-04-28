# Kronos
Kronos is a WASM filter for Envoy intended to add header security inspired by [HelmetJS](https://helmetjs.github.io/) when serving content to the browser with response headers.

## Installation
To deploy via gloo and `wasme`:   
`wasme deploy gloo webassemblyhub.io/haggs/kronos:v0.2 --id=kronos`
via istio and `wasme`:  
`wasme deploy istio webassemblyhub.io/haggs/kronos:latest --id=kronos`

## Features
Currently kronos supports the following headers:
* `X-XSS_Protection: 1`  [X-XSS-Protection](https://wiki.owasp.org/index.php/OWASP_Secure_Headers_Project#xxxsp)
* `X-Frame-Options: SAMEORIGIN`  [X-Frame-Options](https://wiki.owasp.org/index.php/OWASP_Secure_Headers_Project#xfo)
* `X-Content-Type-Options: nosniff`  [X-Content-Type-Options](https://wiki.owasp.org/index.php/OWASP_Secure_Headers_Project#xcto)
* `X-Download-Options: noopen`
* `Strict-Transport-Security: max-age=5184000`. [Strict Transport Security](https://wiki.owasp.org/index.php/OWASP_Secure_Headers_Project#hsts)


## Reference

WASM Hub Link:  
https://webassemblyhub.io/repositories/174/kronos

For more information on security headers see [OWASP Secure Headers Project](https://wiki.owasp.org/index.php/OWASP_Secure_Headers_Project)

To test your website for remediation I recommend the [Key CDN HTTP Header Checker Tool](https://tools.keycdn.com/curl) or comprehensively grade your website with: https://securityheaders.com/

