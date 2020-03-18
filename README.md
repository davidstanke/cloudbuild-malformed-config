# cloudbuild-malformed-config
Repro of how a malformed config can cause strange behavior in Cloud Build

### to reproduce:
1. clone this repo
2. `gcloud builds submit --no-source`

... then go to the build history in GCB. There will be no content in the logs.

Desired behavior: Cloud Build should error out before trying to run a build with malformed image references.
