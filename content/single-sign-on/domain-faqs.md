---
description: Single Sign-on FAQs
keywords: Docker, Docker Hub, SSO FAQs, single sign-on
title: Domains
---

### Can i add sub-domains?

Yes, you can add sub-domains to your SSO , however all email addresses should also be on that domain. Verify that your DNS provider supports multiple txt fields for the same domain.

### Can the DNS provider configure it once for one-time verification and remove it later OR will it be needed permanently?

They can do it one time to add it to a connection. If they ever change IdPs and have to set up SSO again, they will need to verify again.

### Is adding domain required to configure SSO? What domains should I be adding? And how do I add it?

Adding and verifying a domain is required to enable and enforce SSO. Select **Add Domain** and specify the email domains that's allowed to authenticate through your server. This should include all email domains users will use to access Docker. Public domains are not permitted, such as gmail.com, outlook.com, etc. Also, the email domain should be set as the primary email.

### If users are using their personal email, do they have to convert to using the Org’s domain before they can be invited to join an Org? Is this just a quick change in their Hub account?

No, they don't. Though they can add multiple emails to a Docker ID if they choose to. However, that email can only be used once across Docker. The other thing to note is that (as of January 2022) SSO will not work for multi domains as an MVP and it will not work for personal emails either.

### Since Docker ID is tracked from SAML, at what point is the login required to be tracked from SAML? Runtime or install time?

Runtime for Docker Desktop if they configure Docker Desktop to require authentication to their org.

### Do you support IdP-initiated authentication (e.g., Okta tile support)?

We don't support IdP-initiated authentication. Users must initiate login through Docker Desktop or Hub.