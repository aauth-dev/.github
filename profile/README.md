# AAuth

**Authentication & Authorization for Autonomous Agents**

AAuth is an authorization protocol where every agent — any HTTP client — has its own cryptographic identity. No pre-registration. No shared secrets. No dependency on a particular server.

- [aauth.dev](https://www.aauth.dev) — website
- [Protocol draft](https://dickhardt.github.io/AAuth/draft-hardt-aauth-protocol.html) — IETF Internet-Draft
- [playground.aauth.dev](https://playground.aauth.dev) — try it live
- [explorer.aauth.dev](https://explorer.aauth.dev) — protocol explorer app

## Why AAuth?

OAuth 2.0 and OIDC assume every client pre-registers with every authorization server and holds service-issued credentials. That model breaks down for agents that are created on demand, run ephemerally, and discover resources at runtime.

AAuth takes a different approach:

- **Agents prove identity with their own keys** via [HTTP Message Signatures (RFC 9421)](https://www.rfc-editor.org/rfc/rfc9421), published at a well-known URL
- **Every request is signed** — proof-of-possession makes stolen tokens useless without the private key
- **No pre-registration** — resources and authorization servers learn about agents at runtime
- **Progressive adoption** — each party can add AAuth support independently of the others

## Contributing

Issues and PRs welcome on any repo. For protocol-level discussion, open an issue at [dickhardt/AAuth](https://github.com/dickhardt/AAuth).
