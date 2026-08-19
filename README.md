# loomis-redirect

OAuth landing page for the Loomis desktop app. Supabase redirects here after
Google sign-in; the page forwards the session fragment (`#access_token=…`)
straight to the app via the `loomis://auth` deep link and shows an
"Open Loomis" button as a fallback.

Hosted on GitHub Pages. To point sign-in at this page, set the Supabase
`redirect_to` to this page's URL instead of `loomis://auth` — the fragment is
passed through untouched, so the app's callback parsing is unchanged.
