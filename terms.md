# ⚖️ Terms of Service
Last updated : October 2025
Service name : FactoriCord
Owner : Private software suite maintened by the FactoriCord Team

# 1. Introduction

Welcome to **FactoriCord**.
These Terms Of Service ("Terms", "Agreement") govern your access to and use of the FactoriCord ecosytem, which includes :
- The **Central API**
- The **API Client (Agent)**
- The **Discord Bot**
- The **Factorio Mod (LUA)**

By using any part of FactoriCord, you agree to be bound by these Terms.
If you not agree, you must not use or install the Service.

[Discord Terms of Service](https://discord.com/terms)
[Factorio Terms of Service](https://www.factorio.com/terms-of-service)

# 2. Description of the Service

FactoriCord is a **decentralized SaaS platform** that connects **Factorio servers** to **Discord**.
It allows automatic synchronization of in-game events (joins, deaths, chat, etc.) to Discord channels managed
by FactoriCord bot.

The Service consists of :
- A **central coordination API** hosted by the FactoriCord Team
- A **client agent** running on the user's VPS (communicating through secure HTTPS requests)
- A **Discoord bot** integrated with the use's Discord server
- A **Factorio mod** responsible for local data collection (logs only)

The platform is provided **"as-is"**, without warranty of uninterrupted operation.


# 3. Eligibility and Account Linking

To use FactoriCord :
- You must be the owner or administrator of the Discord server where the bot is installed.
- You must have access to a **VPS or dedicated server** running Factorio.
- By registering via the ``!register`` command, you authorize the creation of a unique **server token** linking your Discord server and your Factorio server.

Each token is :
- **Unique** per Discord-Factorio pair
- **Non-transferable**
- **Revocable** at any time by the FactoriCord Team in case of abuse or violation

The registration and linking process operates as follows :
1. The user **invites the bot** to a Discord server.
2. The user runs the ``!register`` command.
3. The bot calls the **Central API**, which generates a **unique server token**.
4. The API responds with this token, securely linked to the Discord guild.
5. The bot displays a personalized installation command for the user’s VPS.
6. The user runs the installer, which:
    - Installs required dependencies (Python)
    - Downloads the Client API source folder
    - Sets up a systemd service
7. The Client API authenticates to the Central API using the token, completing the registration.
8. From then on, the bot relays in-game events from the linked Factorio server to Discord.

This onboarding flow forms part of the contractual use of FactoriCord.
By completing it, the user explicitly agrees to data processing and linkage as described in the Privacy Policy



# 4. Acceptable Use Policy

You agree **not to** use FactoriCord for :
- Illegal, abusivve, or harmful activites
- Spamming or exploiting Discord's API
- Attempting to reverse engineer, resell, or redistribute the proprietary parts of the software (API or client)
- Falsifying registration data or impersonating other servers

You also agree to :
- Keep your **server token** private and secure
- Respect **Discord's Terms of Serice** and **Factorio's EULA**

Violation of these terms may result in immediate suspension or permanent ban.


# 5. Intellectual Property

All software and components of the FactoriCord ecosystem, including, but not limited to the **Central API, API Client** and **Discord Bot** are proprietary and protected under applicable copyright and trade laws.
- The **Factorio Mod** may be partially open-source for transparency and compatibility.
- You are granted a **non-exclusive, revocable license** to use the software solely for integration with your own server.
- You **may not** copy, modify, distribute, or sell any component of FactoriCord without explicit permission.

# 5.1 Client API Distribution

The **API Client (Agent)**  is distributed in **readable source code form**.
It is provided to users exclusively for installation on their own server or VPS as part of the FactoriCord ecosystem.

You are granted a **limited, non-transferable license** to:
- Install and run the Client API as intended by the onboarding process
- Modify it locally for debugging or adaptation, **without redistribution**
- Inspect or audit the code for **transparency** and security verification

You are **not allowed** to:
- Redistribute, republish, or host the Client API for third parties
- Create derived or competing services using its code
- Remove or alter copyright notices

The Client API remains **intellectual property of the FactoriCord Team**, even when distributed in source-readable form.


# 6. Data Handling

FactoriCord collects and processes limited metadata as described in the Privacy Policy, including :
- Discord server identifiers
- Registration tokens
- Lightweight event summaries

All raw logs remain stored on your VPS.
You retain ownershipp of your data.
FactoriCord acts only as a processing and relay service.


# 7. Service Availability and Updates

- The central API may experience maintenance or downtime without prior notice.
- The API Client periodically checks for updates and may automatically download new releases from the secure endpoint.
- Updates are signed and version-checked to ensure compatibility and integrity.

We reserve the right to modify or discontinue features at any time.

Since the Client API is distributed as source code, users are responsible for ensuring local integrity,
permissions, and runtime environment security.

FactoriCord provides signed source archives and official installation
scripts but does not guarantee compatibility with modified or third-party builds.


# 8. Termination

You may stop using FactoriCord at any time by :
- Removing the bot from your Discord server, and/or
- Stopping and uninstalling the client agent on your VPS.

The FactoriCord Team may suspend or terminate access without notice if :
- You breach these Terms
- Your server engages in abuse or unauthorized modification
- Technical or security issues require it

Upon termination, your server token and stored metadata are deleted according to the Privacy Policy.


# 9. Disclaimer of Warranties

FactoriCord is provided **"as-is"** and **"as-available"** without any express or implied warranties, including :
- Fitness for a particular purpose
- Non-infringement
- Continous availability

We make no guarantess regarding uptime, feature completeness, or compatibility with third-party modifications.


# 10. Limitation of Liability

To the maximum extent permitted by law, the FactoriCordd Team shall **not be liable** for :
- Any loss of data, revenue, or profits
- Service interruptions or malfunctions
- Indirect or consequential damages arising from the use of the Service

Your use of FactoriCord is entirely at your own risk.


# 11. Modifications to the Terms

We may update these Terms periodically.
Continued use of the Service after changes take effects constitutes acceptance of the revised Terms.


# 12. Governing Law and Jurisdiction

These Terms are governed by and construed in accordance with the laws of **France**.
Any disputes shall be resolved before the competent courts of **Lyon, France**.


# 13. Contact

For legal or technical inquiries, contact us via :
[👉 Join the official FactoriCord Discord](https://discord.gg/nhXebNj5AZ)