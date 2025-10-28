# 🛡️ Privacy Policy
Last updated : October 2025
Service name : FactoriCord
Owner : Private software suite maintened by the FactoriCord Team

# 1. Introduction

FactoriCord ("we", "our", "the Service") provides a decentralized SaaS platform that connects **Factorio servers**
with **Discord** through a set of coordinated components :
- The **Central API**
- The **API Client (Agent)** installed on the user's VPS
- The **Discord Bot**
- The **Factorio Mod** (LUA) installed on the user's VPS and the user's local machine (Factorio constraints itself)

This privacy policy describes how we collect, use, store, and protect your data when you use any part of the FactoriCord ecosystem.

By using FactoriCord, you agree to this policy.

[Discord Privacy Policy](https://discord.com/privacy)
[Factorio Privacy Policy](https://www.factorio.com/privacy-policy)

# 2. Overview of Data Flow

FactoriCord is **decentralized by design :**
- The **Factorio Mod** and **API Client** run on the user's infrastructure.
- The **Central API** only receives lightweight metadata and event summaries necessary for synchronization.
- No gameplay logs, IP addesses, or chat histories are permanently stored or analyzed.

All transmissions between the client, bot, and API occur over **HTTPS secured channels**.

> The Client API is open in readable source form to allow transparency and user control.
> It performs no hidden telemetry, and only communicates with the Central API using a token-based HTTPS protocol.

# 3. Data Collected and Stored

### A. Server Registration Data
When a user registers a new link between a Discord server and a Factorio server, we collect and store :

| Field | Description | Purpose |
| ----- | ----------- | ------- |
| ``token`` | Unique token per Discord-Factorio pair | Authentication and linkage |
| ``discord guild name`` | Discord server name | Identification |
| ``discord guild ID`` | Discord server ID | Identification |
| ``discord category ID`` | ID of category auto-created by the bot | Channel management |
| ``discord log channel ID`` | Channel for event logs | Event routing |
| ``discord chat channel ID`` | Channel for ingame chat bridge | Communication |
| ``discord admin channel ID`` | Channel for admin notices | Administrative purpose |
| ``discord admin webhook URL`` | Webhook endpoint for admin messages | Notification system |
| ``lastSeen`` | Timestamp of last client communication | Status tracking |
| ``os`` | Client operating system (e.g, Linux, Windows) | Distributing the correct client folder |
| ``clientVersion`` | Installed client version | Update management |
| ``banned`` | Boolean flag | Abuse prevention |
| ``linked agent`` | Boolean flag indicating if a client is linked | Health monitoring |
| ``created at`` | Registration date | Auditing and version tracking |

### B. Event Data

The **API Client** reads Factorio logs locally which are written by the mod, and transmits **structured event summaries** only.
For each event, the following fields may be processed :

| Field | Description |
| ----- | ----------- |
| ``eventType`` | Type of event (e.g, ``player_join``, ``player_died``) |
| ``player`` | Player name or identifier (in Factorio) |
| ``tick`` | In-game tick count |
| ``timestamp`` | Real-worl time of event (based on the file creation data due to Factorio LUA engine limitation) |
| ``data`` | Context specific attributes depending on event type |

**Exemples of contextual data :**
For ``player_died`` :
- ``cause``
- ``total_deaths``
- ``session_deaths``

For ``player_left`` :
- ``session_deaths``
- ``total_deaths``
- ``session_length_ticks``
- ``session_length_seconds``
- ``session_length_formatted``
- ``session_days``

No personnaly identifiable information (PII) is collected from players.

# C. Client API Distribution Data

When installing the Client API through the onboading process, we may record :
- The **client version** and **operating system** used
- The **timestamp** of installation or update
- The **server token** used for verification

No additional metadata or telemetry is collected from the client's system.
The source code is executed locally on the user's VPS
**No system or network data** (such as IP addresses, users, or configuration files) is transmitted beyond the registration handshake.

# 4. Purpose of Processing

The collected data is used exclusively to :
- Authenticate and maintain the link between your Factorio and Discord servers
- Display real time in-game events in Discord (with +/- 10 secs of latency)
- Manage version compatibility between clients and the central API
- Detect and prevent abuse or misconfiguration

No data is sold, shared, or analyzed for commercial purposes.


# 5. Data Retention

| Type | Retention |
| ---- | --------- |
| Server registration metadata | Kept as long as the link (token) is active |
| Event data | Stored temporarily for queueing, deleted once processed for bot |
| Logs | Minimal, rotated automatically for debugging purposes |
| Client-side data | Fully under user control, stored on user VPS, deleted once consumed by client |

You may request removal of your registration data by contacting support (see Section 10).


# 6. Data Security
- All communication occurs via **HTTPS**.
- Tokens are randomly generated with specific salt and stored.
- Access to administrative webhooks or logs is **restricted** to authorized staff only.
- The **API Client** runs in isolation on the user's server. We never access your machine or logs remotely. And we never ask for it.


# 7. Cookies & Analytics

FactoriCord does not use cookies, trackers, or third-party analytics.
No web-based dashboard currently collects visitor data.


# 8. Discord Data Compliance

FactoriCord operates under the **Discord Developer Terms of Service**.
We only store identifiers and metadata necessary for the bot to function.
Messages and chat logs are not persisted or analyzed outside the chat bridge context.


# 9. Factorio Mod Behavior

The LUA mod embedded in your Factorio installation :
- Writes events to local log files
- Does not transmit data directly to the Internet
- Does not communicate directly with the API client. Only through log files.

The mod is transparent and contains no remote execution or telemetry capabilities.

# 10. Your Rights (GDPR)

Under the **General Data Protection Regulation (GDPR)**, you have the right to :
- Access the data stored about your linked servers
- Request deletion or anonymization of your metadata
- Withdraw consent and unregister your server

To exercies these rights, contact us via our support Discord.


# 11. Contat & Support

For privacy inquiries, deletion requests, or security concerns :
[👉 Join the official FactoriCord Discord](https://discord.gg/nhXebNj5AZ)


# 12. Updates to This Policy

We may update this Privacy Policy from time to time.
All changes will be announced via the official Discord and / or the bot.

