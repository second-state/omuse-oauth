# OMuse OAuth relay

Google sends the user here after they approve OMuse's access to their Google Calendar or Drive. Every OMuse box has
its own address, and Google only accepts registered redirect addresses, so this one fixed page forwards Google's
one-time code to the box that started the sign-in (named in the OAuth `state`, which the box created and checks).
The box exchanges the code with PKCE, so a code is useless to anyone else. The page stores nothing.

Published with GitHub Pages at https://second-state.github.io/omuse-oauth/ — register that address as an
authorized redirect URI on the Google OAuth client. The source of truth is
[`deploy/oauth-relay/index.html`](https://github.com/second-state/omuse/blob/main/deploy/oauth-relay/index.html) in
second-state/omuse.

## Other pages
- [`home.html`](https://second-state.github.io/omuse-oauth/home.html) — OMuse's application home page (Google's Branding form).
- [`privacy.html`](https://second-state.github.io/omuse-oauth/privacy.html) — privacy policy.
- [`terms.html`](https://second-state.github.io/omuse-oauth/terms.html) — terms of service.
