# Splash (Splashthat)

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

Splash is an event marketing platform that helps companies market, manage, and measure their live, virtual, and hybrid event programs. Brands and agencies use Splash to build event registration pages, manage guest lists, handle on-site check-in, process ticketing, and analyze event performance across their entire event program.

## API

The Splash REST API (v2.2) is available at `https://api.splashthat.com` and documented at [api-docs.splashthat.com](https://api-docs.splashthat.com/). The API uses OAuth 2.0 client credentials flow. A Client ID and Client Secret are required and are provisioned by the Splash Customer Success team.

### Key Resources

| Resource | Description |
|---|---|
| `/oauth/v2/token` | Obtain and refresh OAuth 2.0 access tokens |
| `/events` | List, retrieve, and update events |
| `/crm/events` | Create events programmatically (requires special API key) |
| `/groupcontacts` | Create, retrieve, and update event guests |
| `/contacts` | Manage organization-level contact records |

### Authentication

API access requires a Client ID and Client Secret obtained from your Customer Success Manager. Credentials are delivered via secure messaging. Use the `/oauth/v2/token` endpoint to exchange credentials for a bearer token; reuse the token across requests rather than re-authenticating on each call.

### Rate Limits

- 2 requests per second
- 250 requests per 15-minute bucket
- 1,000 requests per hour
- Daily limit varies by plan; contact your CSM for specifics
- HTTP 429 returned on rate limit breach; `RateLimit-Reset` header gives retry delay in seconds
- HTTP 503 returned on daily limit breach; syncing resumes the next day
- Webhooks (Simple Postback) do NOT count against API quota

## Plans and Pricing

Splash uses custom annual pricing with no publicly listed tiers. Market data indicates annual spend ranges from $12,500 to $36,500+, with a median around $27,000. API access is available on Enterprise plans. Additional fees include per-ticket transaction fees (2.9% + $0.30), a platform fee (2% + $1.00 per ticket), onboarding fees ($1,500–$12,000), and implementation fees ($2,500–$7,500).

For pricing details, visit [splashthat.com/pricing](https://splashthat.com/pricing).

## Links

- API Documentation: https://api-docs.splashthat.com/
- Support: https://support.splashthat.com/
- Blog: https://splashthat.com/blog
- Status: https://status.cvent.com/
- Integrations: https://splashthat.com/platform/integrations
- Pricing: https://splashthat.com/pricing
- Security: https://splashthat.com/security
