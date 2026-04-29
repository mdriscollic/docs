# FOLIO Documentation

Copyright (C) 2017-2026 The Open Library Foundation

This software is distributed under the terms of the Apache License,
Version 2.0. See the file "[LICENSE](LICENSE)" for more information.

## Introduction

This is the documentation for FOLIO apps.
If working with this Hugo site locally, be sure to execute

```
git submodule update --init --recursive
```

before attempting to build with Hugo for the first time.

### Serve with Docker
One way to locally serve the site is with Docker

1. [Install Docker for your operating system](https://docs.docker.com/get-docker/)
2. From the docs directory, run
```
docker run --rm -it -v $(pwd):/src -p 1313:1313 klakegg/hugo:ext-alpine server
```

### Serve locally with Hugo
Another option is to run Hugo locally on your computer

1. [Install Hugo for your operating system](https://gohugo.io/getting-started/installing)
2. From the docs directory, run
```
hugo server -D
```
### Preview the Docs site
After serving, visit <http://localhost:1313>

## FOLIO Documentation Working Group

Community members who are interested in helping with documentation should reach out to a member of the FOLIO Documentation Working Group to find out how you can help.

For questions regarding documentation, please join the
[slack channel](https://folio-org.atlassian.net/wiki/spaces/COMMUNITY/pages/4227287/FOLIO+Communication+Spaces#FOLIOCommunicationSpaces-slackSlack)
#folio-documentation and ask there.

Please refer to the
[FOLIO Documentation Working Group webspace](https://folio-org.atlassian.net/wiki/spaces/SS/pages/4489616/FOLIO+Documentation+Working+Group)
that includes the
[Basic Workflow in Github for Updating Existing Documentation](https://folio-org.atlassian.net/wiki/spaces/SS/pages/4490218/Basic+Workflow+in+Github+for+Updating+Existing+Documentation).

## Issue tracker

See project [DOCS](https://issues.folio.org/browse/DOCS)
at the [FOLIO issue tracker](https://dev.folio.org/guidelines/issue-tracker).

