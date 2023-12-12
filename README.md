# realtimate-sample-multiple-atlas-app-service

> This is a demo of `realtimate` when using multiple atlas at once

## Steps to create this repository

- `npm init`
- `npx realtimate new`
- `npx realtimate genrate app1`
- `npx realtimate genrate app2`

this will also create a Github action and CI to allow automatic deploy on your atlas environements. the CI requires the following secrets:

- `REALM_API_PUBLIC_KEY` and `REALM_API_PRIVATE_KEY` for using the atlas cli
- `REALM_PROJECT` for using the right project (you can get it via the url, when using the atlas apps service gui)
- A private access token, you'll need to create a private app in your organisation (in the `build.yml` -> `MERGE_APP_ID` and `MERGE_PRIVATE_KEY`)

`build.yml` handles creating appservices in the atlas context
`clean.yml` removes the app once the pr is merged