# WellSaid Labs (wellsaid-labs)

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

WellSaid Labs is an AI text-to-speech (TTS) platform that turns text into studio-quality synthetic voiceover using a library of 200+ AI voice avatars across many styles, languages, and accents. Beyond the AI Voice Studio web app, WellSaid exposes a documented REST API (base `https://api.wellsaidlabs.com/v1`) that renders text to speech, streams audio for low time-to-first-byte playback, returns word-level timing and subtitles, manages asynchronous clips, lists voice avatars, and lets teams control pronunciation with replacement libraries and respelling suggestions.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/wellsaid-labs/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/wellsaid-labs/refs/heads/main/apis.yml)

## Access Model

API access is gated, not open self-serve. Developers create a free WellSaid account, request a **trial API key**, and then work with WellSaid to land on a **business plan** for production use. Requests authenticate with an `X-Api-Key` header, and WellSaid states it does **not currently support end-user authentication**, recommending that calls be made from an internal or trusted source. Default keys are limited to **3 requests per second** and **1,000 characters per request**, plus a **monthly character quota**; higher concurrency is available on request. Rate-limit and quota state is returned on `x-rate-limit-*` and `x-quota-*` response headers.

The endpoints, request fields, and response shapes in the OpenAPI here are modeled from the public documentation at docs.wellsaidlabs.com and are honestly approximated where the reference does not publish a full JSON schema.

## Tags

- AI
- Text to Speech
- TTS
- Voice
- Voiceover
- Speech Synthesis
- Audio

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### WellSaid Labs Text-to-Speech API

Render text to speech and receive the audio as an HTTP stream for low time-to-first-byte playback, or render with word-level timing and subtitle output. Requests take the text, a `speaker_id` (voice avatar), and an optional model, authenticate with an `X-Api-Key` header, and return MP3 audio. Limited by default to 1,000 characters per request.

- **Human URL:** [https://docs.wellsaidlabs.com/reference/getting-started-with-your-api](https://docs.wellsaidlabs.com/reference/getting-started-with-your-api)
- **Base URL:** `https://api.wellsaidlabs.com/v1`

#### Tags

- Text to Speech
- TTS
- Streaming
- Renders

#### Properties

- [Documentation](https://docs.wellsaidlabs.com/docs/getting-started)
- [API Reference](https://docs.wellsaidlabs.com/reference/getting-started-with-your-api)
- [OpenAPI](openapi/wellsaid-labs-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wellsaid-labs.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wellsaid-labs.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WellSaid Labs Clips API

Create text-to-speech clips asynchronously, list recent clips, fetch a single clip by id, and combine a list of clips into a single audio file with pauses between them. Useful for longer-form voiceover production where renders are assembled from many segments.

- **Human URL:** [https://docs.wellsaidlabs.com/reference/getting-started-with-your-api](https://docs.wellsaidlabs.com/reference/getting-started-with-your-api)
- **Base URL:** `https://api.wellsaidlabs.com/v1`

#### Tags

- Clips
- Async
- Rendering

#### Properties

- [Documentation](https://docs.wellsaidlabs.com/docs/getting-started)
- [API Reference](https://docs.wellsaidlabs.com/reference/getting-started-with-your-api)
- [OpenAPI](openapi/wellsaid-labs-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wellsaid-labs.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wellsaid-labs.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WellSaid Labs Voice Avatars API

List the available voice avatars with their metadata - the numeric speaker id, avatar name, style (Narration, Promo, Conversational, Character), language, accent, descriptive characteristics, and compatible models - so a client can pick the right voice for a text-to-speech render.

- **Human URL:** [https://docs.wellsaidlabs.com/reference/available-voice-avatars](https://docs.wellsaidlabs.com/reference/available-voice-avatars)
- **Base URL:** `https://api.wellsaidlabs.com/v1`

#### Tags

- Voices
- Avatars
- Catalog

#### Properties

- [Documentation](https://docs.wellsaidlabs.com/reference/available-voice-avatars)
- [API Reference](https://docs.wellsaidlabs.com/reference/getting-started-with-your-api)
- [OpenAPI](openapi/wellsaid-labs-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wellsaid-labs.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wellsaid-labs.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WellSaid Labs Pronunciation API

Manage pronunciation across renders. Create and manage replacement libraries and the individual replacements inside them so brand names, acronyms, and jargon are spoken consistently, and fetch respelling suggestions that help coax the correct pronunciation of a difficult word.

- **Human URL:** [https://docs.wellsaidlabs.com/reference/getting-started-with-your-api](https://docs.wellsaidlabs.com/reference/getting-started-with-your-api)
- **Base URL:** `https://api.wellsaidlabs.com/v1`

#### Tags

- Pronunciation
- Replacement Libraries
- Respelling

#### Properties

- [Documentation](https://docs.wellsaidlabs.com/docs/getting-started)
- [API Reference](https://docs.wellsaidlabs.com/reference/getting-started-with-your-api)
- [OpenAPI](openapi/wellsaid-labs-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wellsaid-labs.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wellsaid-labs.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/wellsaid-labs)
- [Website](https://wellsaidlabs.com)
- [Documentation](https://docs.wellsaidlabs.com/docs/getting-started)
- [Plans](plans/wellsaid-labs-plans-pricing.yml)
- [Rate Limits](rate-limits/wellsaid-labs-rate-limits.yml)
- [Fin Ops](finops/wellsaid-labs-finops.yml)

## Review

Does WellSaid Labs expose a documented public WebSocket API? **No.** WellSaid's public API is request/response REST over HTTPS authenticated with an `X-Api-Key` header. Its `POST /tts/stream` endpoint returns a chunked stream of the MP3 audio (not the finished file) for low time-to-first-byte, but that is HTTP response streaming - not a WebSocket (`wss://`) or Server-Sent Events channel. No AsyncAPI document was authored. See [review.yml](review.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
