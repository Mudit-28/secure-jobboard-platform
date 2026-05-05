# 🔐 Secure JobBoard Platform
> Production-grade recruitment platform where security is a first-class concern 
at every layer — from HTTPS termination to end-to-end encrypted messaging.

A full-stack job board connecting employers and job seekers, built with React 
and Django. Every sensitive asset is protected — resumes are encrypted at rest 
with **Fernet (AES-128-CBC + HMAC)**, messages are **end-to-end encrypted using 
RSA-2048 + AES-GCM** (the server never sees plaintext), and every significant 
action is recorded in a **SHA-256 hash-chained audit log** that makes tampering 
detectable.

## Key Features
- 🔒 E2E encrypted messaging — RSA-2048 key exchange + AES-GCM per message
- 📁 Fernet-encrypted resume storage — plaintext never written to disk  
- 🔑 OTP-based email verification with 5-minute expiry
- 📋 SHA-256 hash-chained audit log with admin chain-verify endpoint
- ⚡ Real-time chat over WSS via Django Channels + Redis
- 👥 Role-based dashboards for employers and job seekers
- 🌐 Nginx reverse proxy with HTTPS enforce
