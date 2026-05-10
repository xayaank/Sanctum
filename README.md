Sanctum — SecCRY Encrypted Chat
SecCRY Encrypted Chat — Private, Peer-to-Peer, Forward-Secret

Project Overview
Sanctum is a high-security, CLI chat application built on modified SecCRY cryptographic primitives. It enables users to host and join private chat rooms directly from their computers without relying on third-party servers. Every message is encrypted end-to-end, ensuring that only the participants in the room can read the conversation.

Security Architecture
X25519 ECDH (Perfect Forward Secrecy): Sanctum generates ephemeral session keys for every connection. Even if the room password is compromised later, past conversations remain unreadable because the session keys are never stored.

AES-256-GCM (Authenticated Encryption): All message traffic is secured using AES-256-GCM, providing both confidentiality and data integrity. Each message uses a fresh Initialization Vector (IV).

Argon2id (Robust Key Derivation): The system utilizes Argon2id for secure password-based authentication challenges and chat log encryption.

Core Features
Serverless P2P: Traffic moves directly between participants; no middleman servers are involved.

Encrypted Whispers: Send private messages (/w) to specific users that are only visible to the sender and recipient.

Flexible Logging: Export chat history as plain text or as encrypted .SCRY files compatible with the SecCRY 3.0.0 suite ONLY.

Heartbeat Monitoring: Automated pings ensure the room stays clean by dropping inactive or disconnected clients.

License: PolyForm Noncommercial 1.0.0 (see LICENSE file for full terms)

Core Contributors: Ayaan Khan (Lead Developer & Publisher) - Suleiman Sheikh (Contributor) - Raymond Kelly (Contributor) - Rajesh Patel (co-author of SecCRY 3.0.0)
