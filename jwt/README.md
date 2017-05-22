

# JWT 

Floyd Kosch - Creative thinking, Inc.
floyd@oedna.com

http://bit.ly/2qMsdNd

https://jwt.io

[JWT Debugger](https://jwt.io/#debugger)
[Chrome JWT Debugger](https://chrome.google.com/webstore/detail/jwt-debugger/ppmmlchacdbknfphdeafcbmklcghghmd)

[JWT Validation and Authorization in ASP.Net Core](https://blogs.msdn.microsoft.com/webdev/2017/04/06/jwt-validation-and-authorization-in-asp-net-core/)


https://auth0.com

https://tools.ietf.org/html/rfc7519

[Presentation - Generating a JWT](http://focusagent.oedna.com/info/signing.html)




JWT : {
    HEADER,
    PAYLOAD,
    SIGNATURE
}

Header is defined by 7519:
HEADER: {
    "alg", "HS256",
    "typ" : "JWT"
}
Warning: Because the header can be hacked, the algorithm coudl be a maliciosu attempt to trick

Payload 
{
    "sub": "123", -- id of security prioncipal
    "exp": 44455545444, -- expiration, a javascript timestamp
    "iss": "oedna" --issuer: your domain name, your URN, your IDP
}

HEADER.PAYLOAD are run through HMACSHA256

HEADER.typ: ['JWT', 'JWE', 'none'] 
PAYLOAD Reserved Properties:
iss
sub - subject if token, the SSID, User ID
aud - audience
iat - issued-at timestamp
exp - expire timestamp
ndf - not-before timestamp
jti - JWT Token ID - Unique Token ID, for replay prevention




## My own notes, nothign to do with presentation
### ASP.Net Core and JWT
https://blogs.msdn.microsoft.com/webdev/2017/04/06/jwt-validation-and-authorization-in-asp-net-core/

### WIF 4.5+

https://msdn.microsoft.com/en-us/library/hh377151.aspx

### WIF Pre 4.5
https://msdn.microsoft.com/en-us/library/ee517296.aspx

### Thinktecture

http://stackoverflow.com/questions/31656373/how-to-use-thinktecture-identityserver-3-in-web-api-2

[Hello World Example of Setting up an Identity Server](https://identityserver.github.io/Documentation/docsv2/overview/simplestOAuth.html)


http://stackoverflow.com/questions/34789950/implement-identity-server-authentication-in-real-world-scenario

https://www.codeproject.com/Articles/683732/Thinktecture-Identity-Server-Configuration-Customi


