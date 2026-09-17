# VSR Tool — Ventilator Settings Record
**Sleep & Ventilation Department · Royal Brompton Hospital / GSTT**

A phone-friendly web app for capturing ventilator settings at the bedside and generating a Ventilator Settings Record to send to Baywater Healthcare.

---

## What it does

1. **Photograph** the ventilator settings screen, alarms panel, serial number label, and barcode
2. **AI extracts** all visible settings automatically — mode, IPAP, EPAP, Ti, backup rate, rise time, trigger, cycle, alarms, serial number, asset number
3. **Review** the extracted data on screen and correct anything if needed
4. **Download** a formatted settings record and email it directly to Baywater

Supports:
- Up to 2 devices per record
- Up to 4 profiles/prescriptions per device
- Up to 4 settings screen photos per profile (for devices where settings span multiple screens)
- Change of device or same device (service/prescription change) workflows

---

## Live app

**[https://scutts318.github.io/VSR_phone_app_v3.html](https://scutts318.github.io/VSR_phone_app_v3.html)**

Works on any phone or desktop browser. Can be saved to iPhone/Android home screen for app-like access.

---

## First-time setup

Open the app and enter:

| Field | Value |
|---|---|
| Passphrase | Contact the Sleep & Ventilation team |
| Worker URL | `https://vsr-proxy.scutts318.workers.dev` |
| Your name | Your full name |
| Role | Your job title |
| Hospital | Your hospital |

These are saved to your device — you only need to enter them once.

---

## Devices supported

Tested with:
- Breas NIPPY 4 / NIPPY 4+ / NIPPY 3+
- Löwenstein Prisma / Prisma 40 / Prisma 50-C
- ResMed Lumis 100 / Lumis 150 (iVAPS, AVAPS, S/T modes)
- Philips Trilogy Evo

The AI reads whatever is visible on screen — works with any ventilator interface.

---

## Data & governance

- **No patient data is processed by AI** — only photos of device hardware screens
- Patient name, NHS number, and address are added manually to the accompanying email
- Photos are sent to a secure Cloudflare Worker proxy and then to the Anthropic API
- Nothing is stored — data is processed in memory only

---

## Send completed records to

📧 **bhltd.niv@nhs.net**  
📞 0800 121 4524

---

## Contact

**Steve Cutts** — Band 8a Respiratory Physiotherapist & Clinical Team Lead  
Sleep & Ventilation Department · Royal Brompton Hospital / GSTT  
stephen.cutts@gstt.nhs.uk
