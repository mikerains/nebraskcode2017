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




