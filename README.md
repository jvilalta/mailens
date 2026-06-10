# Mailens

Mailens is a protocol-agnostic mail access gateway that sits in front of existing email providers and exposes a unified, policy-controlled view of a mailbox.

It currently focuses on IMAP compatibility, with planned support for JMAP and other mail access protocols.

## What it does

Mailens acts as a virtual mail layer between your email provider and your mail client:

- Connects to existing providers (e.g. Gmail, Fastmail, IMAP servers)
- Applies user-defined rules and policies (e.g. whitelist-only inboxes)
- Exposes a filtered mailbox via standard protocols
- Maintains a consistent, provider-agnostic mail model

## Goals

- Unified mail access across providers and protocols
- Fine-grained control over what messages are visible
- Extensible architecture for IMAP, JMAP, and future protocols
- Minimal friction for existing mail clients

## Architecture (high level)

Mail Client (IMAP/JMAP)
        ↓
     Mailens
        ↓
Provider adapters (Gmail / Fastmail / IMAP / etc.)

Mailens normalizes all mail into a common internal model and applies policy before exposing it to clients.

## Status

Early-stage design / prototype.

## License

MIT
