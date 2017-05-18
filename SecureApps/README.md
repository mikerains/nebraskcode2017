# Building Modern Secure Apps
2:15PM Thursday
Mike Douglas, Deviron Consulting, Omaha

What is "Secure"?
- Rick Assessment
  * Risk = Liklihood * impact
  * OWASP Model - they have a Spreadsheet
    * Identify Risk
    * Est
    * Est Impact
    * Determine Sevrity
    *
    *
- How to manage
  * Controls
    * Prevent
    * Detect
    * Correct - help mitigqte one materialized
  * Web Applicaiton Firewalls
    * Have OWASP Top 10 Rules built in
      * Injection,
      * Broken Auth
      * etc etc
  * Encryption
    * TDE - SQL encryption at rest
    * SSL/TLS - Not all SSL is secure.  Checking tool:
        * https://www.ssllabs.com/ssltest/
  * Whitelisting
  * Web.config - IP, IP ranges, FQDN
    <security><ipSecurity allowUnlisted="false" denyAcitonn="notFound">
      <clear>
      <ad ipAddress-"52.86.20.100" allowed = "true"/>
    </security>

# Securing an App
1. Secure Infrastructure
2. Security built in to process
3. Security Monitoring - detect unusual behaviors

## Secure Infrastructure
- Deviron uses Microsoft Azure, because it has security baked-in.  They will detect penetration attacks and shut down the site, you have to coordinate penetration testing.
- Compliant to security certificaitons
- Platform
  * App Service
  * Service FGabrice
  * Azure Container Services
  * IAAS (Infrastructure as a svc)
- Tools
  * App Insights
  * OMS
  * Azure Security center
  * Azure Monitor

### App Insights - smart detection - notice if a user is doing actions not typical

# Securing the App - AuthN and AuthR
- Typical Modern Auth
  * ADFS 4, ID Server, Azure AD
    * Authentication: WS-Fed, SAML2.0, OpenID Connect
    * Authorization: OAuth2
- Authntication Flows
  * Authorization Code Flow (Server to server, key is known by client server)
  * Implicit Flow - redirect client to verify client identity
  * Hybrid Flow
- Authentication Attacks
  * MITM - use HTTP to prevent 
  * CSRF - use Anti-forgery to prevent
  * XSS - Code reads cookie.  Prevent with "httpOnly" flag on cookie.

- Solution: OpenID/OAuth2 + HTTPS
  * don't authe ticate with the cookie
  * require token added to the header
  * use secure flag so it isn't sent to the server
  * do not use httpOnly because cookie needs to be read by javascript
  * use LocalStorage and SessionStorage to store token

# Penetration Tool: OWASP ZAP
https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project
- dynamic scanning of app.
- can be automated in deployment

# Open Source Vulnerabililties - Tool: Whitesource Bolt 
- Integrate with TSF build. 
6 month subscription included with VS Subscription


# Static Code Analysis Tools
## Microsoft DevSkim
- provides inline security analysis
## Checkmarx - 

# Common Issues
X-Frame-Options header not set
2. Incomplete or No cache-control and pragma Header Set
3. cookie No httpOnly flag
4. cookies without secure flag
5. XSS protection not enabled
6.
7.

<httpPtotocol>
<customHeader>
<add name "X-FRAME-Options" vallue="SAMEORIGIN" or "DENIED">
stops IFrame attack

<add name="Cache-Control" value="must-revalidate"

<add name="X-XSS-Protection" value="1"

<add name="X-Content-Type-Options" value="nosniff"
<remove name="X-Powered-By"


<...httprRuntime enableVersionHeaders="false"...
<system.webServer>
<Security>
<requestFiltering removeServerHeadre="true">
</security>
<httpProtocol>
<validation validateIntegratedModeConfiguration="false"
<rewrite>
 <rule>
<action tyope="Redirect" url="https://{HTTP_HOST}/{R:1"}/>
</rewrite>

