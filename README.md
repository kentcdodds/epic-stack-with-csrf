# Epic Stack with CSRF Protection

This is an example of how to integrate the
[`remix-utils`](https://github.com/sergiodxa/remix-utils) package utilities for
[Cross-Site Request Forgery (CSRF)](https://en.wikipedia.org/wiki/Cross-site_request_forgery)
protection with the Epic Stack. The easiest way to explore the example is to
pull up
[the commit history](https://github.com/kentcdodds/epic-stack-with-csrf/commits/main).

Following the steps laid out in the Remix Utils docs is sufficient for this:

1. Install `remix-utils`
2. Generate the authenticity token in the `root.tsx` loader (be certain to
   commit the session to set the cookie)
3. Wrap the App in the `<AuthenticityTokenProvider />` and provide the token
4. Render a Form with the `<AuthenticityTokenInput />` component
5. Verify in the Action using `verifyAuthenticityToken` and the session.
