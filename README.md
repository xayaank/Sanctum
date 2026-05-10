Sanctum — SecCRY Encrypted Chat — Private, Peer-to-Peer, Forward-Secret

Project Overview: Sanctum is a high-security, CLI chat application built on modified SecCRY 3.0.0 cryptographic primitives. It enables users to host and join private chat rooms directly from their computers without relying on third-party servers. Every message is encrypted end-to-end, ensuring that only the participants in the room can read the conversation.

Security Architecture: X25519 ECDH (Perfect Forward Secrecy): Sanctum generates ephemeral session keys for every connection. Even if the room password is compromised later, past conversations remain unreadable because the session keys are never stored.

AES-256-GCM (Authenticated Encryption): All message traffic is secured using AES-256-GCM, providing both confidentiality and data integrity. Each message uses a fresh Initialization Vector (IV).

Argon2id (Robust Key Derivation): The system utilizes Argon2id for secure password-based authentication challenges and chat log encryption.

Core Features: Serverless P2P: Traffic moves directly between participants; no middleman servers are involved.

Encrypted Whispers: Send private messages (/w) to specific users that are only visible to the sender and recipient.

Flexible Logging: Export chat history as plain text or as encrypted .SCRY files compatible with the SecCRY 3.0.0 suite ONLY.

Heartbeat Monitoring: Automated pings ensure the room stays clean by dropping inactive or disconnected clients.

User Commands: `/who` Lists all participants currently in the room. `/w <user> <msg>` Sends an encrypted private message to a specific user. `/clear` Clears the terminal screen for better readability. `/exit` Gracefully leaves the room and opens the chat log saving menu.

DISCLAIMER: Sanctum is provided "as is" without warranty. It has not undergone independent security auditing. The host's IP is visible to participants, and participant IPs are visible to the host. Use at your own risk.

Core Contributors: Ayaan Khan (Lead Developer & Publisher) - Suleiman Sheikh (Contributor) - Raymond Kelly (Contributor) - Rajesh Patel (co-author of SecCRY 3.0.0)

License: PolyForm Noncommercial 1.0.0 (see LICENSE file for full terms)

Copyright (c) 2026 Ayaan Khan.
