# WellSaid Labs (wellsaid-labs)

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
