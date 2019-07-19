# postman-jwt
Demonstrate how to do a Postman JWT without external callouts

JWT authentication is a common requirement for modern APIs. The support in Postman for generating RS256 signed JWTs is pretty poor, but it can be done.

The details are here, and the script in this repo shows how to do it pretty much all inline:

https://medium.com/adobetech/using-postman-for-jwt-authentication-on-adobe-i-o-7573428ffe7f


To use this script, you'll need a private key in PEM-encoded PKCS1 format. Other formats might work too, if CryptoJS etc supports them. PKCS#1 is where you'll see -----BEGIN RSA PRIVATE KEY-----. You can harcode the private key in your source, or include it as a variable - but be careful not to make any included private keys accessible to people who shouldn't have access. Some considerations are here: https://learning.getpostman.com/docs/postman_for_publishers/run_button/security/

You can change the code to format whatever claims you want.
