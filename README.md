# Goose Insurance (goose-insurance)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
