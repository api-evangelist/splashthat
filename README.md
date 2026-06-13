# Splash (Splashthat)

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
