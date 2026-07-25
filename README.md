# Goose Insurance (goose-insurance)

Goose Insurance Services Inc. is a Vancouver, British Columbia based digital insurance distributor — an app-first licensed agency and MGA rather than a carrier — that sells travel medical, Visitors to Canada, term life, whole life, final expense, critical illness, accidental death and dismemberment, hospital cash, kids and renters coverage through the Goose mobile "insurance super app". Founded in 2017 and licensed across British Columbia, Alberta, Saskatchewan, Manitoba, Ontario, Quebec (AMF firm registration 603913), New Brunswick and Nova Scotia, Goose underwrites nothing itself: every policy is placed with a partner carrier. Its home market is Canada, with a US launch in 2020, and it sits in the thin digital-broker layer beneath the Big-Few Canadian oligopoly alongside Zensurance and APOLLO.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/goose-insurance/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/goose-insurance/refs/heads/main/apis.yml)

## Tags

- Insurance
- Canada
- Insurtech
- Life Insurance
- Travel Insurance
- Health Insurance
- Broker
- Digital Distribution
- Managing General Agent
- Mobile

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

None. As of the 2026-07-25 review, Goose Insurance publishes **no public API**.

Every first-party developer hostname and path probed either failed to resolve or returned 404: `developer.`, `developers.` and `docs.gooseinsurance.com` do not resolve at all, and `/developers`, `/api`, `/developer`, `/partners` and `/integrations` on the marketing site all return 404. The site's 125-URL sitemap contains no developer, docs, API, or integration path anywhere.

A host does answer at `https://api.gooseinsurance.com` — Heroku-fronted, returning a bare HTML 404 at the root and at every probed spec path (`/openapi.json`, `/swagger.json`, `/api-docs`, `/docs`, `/redoc`, `/spec`, `/graphql`, `/.well-known/*`). That is the private backend for the Goose mobile app, not a documented product API. No OpenAPI, Swagger, AsyncAPI, GraphQL SDL, `.proto`, or Postman collection exists to harvest, so this repo has no `openapi/` directory.

Nothing on the site references **ACORD, AL3, ACORD XML, NGDS, IVANS, Applied Epic, or Vertafore** — Goose is a direct-to-consumer app rather than an agency-management-system participant, so the ACORD/IVANS download rail does not touch it.

Quote, bind, issue and FNOL all exist as product capability — quoting and buying in seconds from a phone is the entire pitch — but every one of them is consumer-facing inside the app, and none is exposed as an addressable API. Claims are filed through the claims page and the underwriting carrier's own process. No auth model, no webhooks, no event catalog is published.

This is the expected posture for a Canadian D2C insurtech. Canada has no open-insurance mandate — Consumer-Driven Banking excludes insurance entirely — so there is no forcing function to publish quote/bind/issue/FNOL. The product is the app, and the app is the only channel.

See [review.yml](review.yml) for the full probe log with HTTP statuses.

## Underwriting Carriers

Goose places every policy with a partner insurer, per its [partners page](https://www.gooseinsurance.com/en-ca/partners):

- **AIG Canada** — hospital cash and income protection
- **iA Financial Group** — group life, AD&D, critical illness
- **American-Amicable Group** — term life, final expense
- **Teachers Life** (reinsured by Gen Re) — term life
- **TuGo** — travel medical
- **IMG International** — international medical, trip cancellation
- **MSH Group** — kids insurance, COVID-19 products
- **Lloyd's of London** — Visitors to Canada
- **Sutton National** — renters

## Links

- [Website](https://www.gooseinsurance.com/)
- [About](https://www.gooseinsurance.com/en-ca/about)
- [Partners](https://www.gooseinsurance.com/en-ca/partners)
- [Licensing](https://www.gooseinsurance.com/en-ca/licensing)
- [Help Center](https://support.gooseinsurance.com/)
- [Blog](https://www.gooseinsurance.com/en-ca/blog)
- [News](https://www.gooseinsurance.com/en-ca/news)
- [Claims](https://www.gooseinsurance.com/en-ca/claims)
- [Contact](https://www.gooseinsurance.com/en-ca/contact)
- [Careers](https://www.gooseinsurance.com/en-ca/careers)
