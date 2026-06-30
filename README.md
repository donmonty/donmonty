# Hi! Montero here.
I'm a software engineer, marketer, and former entrepreneur. I enjoy building B2B products that solve messy, real-world operational problems. I am always open to work opportunities, so feel free to drop me an email in case you want to connect.

## Featured Projects

## [NubeBar](https://github.com/donmonty/api-nubebar-django)
NubeBar is a mobile app that helps bar managers track their alcohol inventory to prevent theft and boost profits.

Alcohol accounts for at least 40% of total sales for upscale bars and restaurants. Alcohol also has the highest margins and is the most valuable inventory for these businesses. However, they manage their alcohol inventory using manual, time-consuming methods, which make inventory control a big challenge. I designed and built NubeBar to solve this problem.

Thanks to NubeBar's barcode and QR scanner, bar managers can complete full inventory counts in minutes, not hours. And with NubeBar's analytics module, bar managers have a detailed view of their inventory over time. NubeBar highlights any differences between reported sales and actual alcohol consumption, allowing bar managers to uncover theft or malpractice at the bottle level with milliliter precision.

As a solo, bootstrapped founder, I handled customer development, product design, engineering, and sales.

![nubebar-banner](https://user-images.githubusercontent.com/13739454/198862782-abba9349-52ab-48ab-afc9-701d11a7f9ce.png)

### Features

NubeBar allows bar managers to:

- Add new bottles to the inventory with the integrated barcode and QR code scanner.
- Track the liquid volume of each bottle over time.
- Integrate with API-less, point-of-sale software.
- Perform daily inventory counts in minutes
- Create variance analysis reports to compare alcohol sales versus actual consumption
- Detect bogus, counterfeit bottles before adding them to the inventory.
- Review the complete lifecycle of any bottle, including its volume over time from the moment it was stocked up until it was empty.
- Create inventory cost reports
- Manage multiple bar/restaurant locations
- Manage multiple storage locations within a location
- Preload more than 500 spirit brands sold in Mexico
- Detect bogus/counterfeit bottles and prevent their registration in inventory


[Check out the backend repo (Django).](https://github.com/donmonty/api-nubebar-django)

[Check out the mobile app repo (React Native).](https://github.com/donmonty/frontend-nubebar)

[Watch a quick video of the app here](https://www.notion.so/NubeBar-e54b9344880e4a34a0aa655b94def266#a8fd30fa783f478cb3316b7f2561f001)

## [NubeBar Dashboard and Chatbot](https://github.com/donmonty/bar-metrics)
A multi-metric web dashboard and AI chatbot that gives bar managers a real-time view of their inventory and sales health, headlined by inventory shrinkage/variance — the gap between what POS sales say should have been poured and what physical bottle-weighing proves was actually consumed. It's the analytics layer on top of NubeBar's inventory data, turning raw scan/sales data into the insight that actually catches theft, over-pouring, and spillage at the bottle level.

Built as a multi-tenant Next.js app reading from the existing NubeBar production database (owned for writes by a separate legacy Django service), with an AI chatbot that lets managers ask questions about their data in plain language instead of digging through reports.

### Key Features
- **Four drill-down dashboards:** Variance (shrinkage by ingredient), Sales (revenue trend + top-selling recipes), Stock Value (current inventory value by storage location), and Unregistered Products (POS sales the catalog can't attribute — a data-quality/leakage signal) — plus a landing overview composing all four into compact summary cards.
- **Tool-calling AI chatbot (Claude + Vercel AI SDK):** Answers natural-language questions about inventory and sales, with generative UI for rich responses, plus a guarded read-only SQL escape hatch for ad-hoc queries the built-in tools don't cover.
- **Multi-tenant auth & data isolation:** Auth.js magic-link sign-in, bar managers scoped to their own Locations, enforced with Postgres Row-Level Security on top of a locked-down, read-only database role — defense in depth, not just app-layer checks.
- **Safe integration with a live legacy system:** Reads a production database it doesn't own for writes, via an introspected (never hand-edited) schema and a dedicated connection pool, so the dashboard can ship independently without risking the existing Django app.
- **Two-database architecture:** A dedicated app database (Neon Postgres) for dashboard-owned state (users, sessions, location assignments) kept cleanly separate from the read-only legacy data store.

<img width="1411" height="989" alt="Screenshot 2026-06-30 at 12 19 45 a m" src="https://github.com/user-attachments/assets/e53f0b82-2cd1-4c4a-beff-b19cabb76ac1" />
<img width="1411" height="989" alt="Screenshot 2026-06-30 at 12 20 17 a m" src="https://github.com/user-attachments/assets/b1cb9281-e250-4474-9b2e-543165af7575" />
<img width="1411" height="989" alt="Screenshot 2026-06-30 at 12 19 39 a m" src="https://github.com/user-attachments/assets/de381fc5-32ef-4def-bb8e-b4badb882c42" />


## Axle Health: Clinician Mobile App
[Axle Health](https://www.axlehealth.com/) is a YC-backed healthcare technology company that helps enterprise healthcare providers improve clinician workforce productivity through scheduling, route optimization, and patient engagement software.
 
I worked with the founding team to help build Axle’s first mobile app MVP, focused on helping clinicians manage and complete patient visits in the field.

<img width="1784" height="924" alt="Axle 01" src="https://github.com/user-attachments/assets/6f2f8cea-9c25-4878-aaa7-46960665da39" />
<img width="1784" height="940" alt="Axle 02" src="https://github.com/user-attachments/assets/4c56c9c4-fd26-433d-8efb-f834a2d5b636" />

### Highlights
- Built core mobile app functionality for clinicians fulfilling scheduled patient visits. 
- Developed features that allowed dispatchers to track clinician location in real time. 
- Helped clinicians visualize and manage their visit schedules over time. 
- Built visit detail views showing patient information, location details, and required tasks. 
- Implemented task workflows that allowed clinicians to review instructions, submit proof of completion, and add notes per visit.

### Impact
- Helped Axle move from operational workflows toward a dedicated mobile product for field clinicians. 
- Contributed to an early product foundation for real-time clinician coordination, visit tracking, and task completion.

## Curri: Driver Mobile App Revamp
[Curri](https://www.curri.com/) is a YC-backed logistics marketplace that connects truck drivers with companies that need to deliver construction and industrial supplies.

<img width="1327" height="893" alt="Curri Routes" src="https://github.com/user-attachments/assets/b8c23755-2490-4aea-9375-70401df85945" />


Curri was transitioning from a legacy delivery data model to a newer, more powerful route-based model. The new model was more flexible and better aligned with the company's future, but the driver app used by thousands of marketplace drivers was still built around the legacy model.

This created a difficult migration challenge. The driver app needed to support the new route-based fulfillment flow, but the rest of the delivery system still depended on the legacy model. Rebuilding the app around the new model could not come at the cost of breaking backward compatibility or disrupting active marketplace operations.

At the same time, the driver app still had to preserve the core workflows drivers relied on every day: viewing their work, completing stops, uploading photos, collecting signatures, writing notes, and providing proof of delivery for customer orders.

### Highlights
- Built a new fulfillment flow inside the existing React Native driver app, powered by the new route-based data model and supported by a translation layer that kept the old and new models in sync.
- Created a translation layer that kept legacy deliveries and new route data in sync, enabling a gradual migration without disrupting live operations.
- Implemented proof-of-delivery workflows including photo uploads, customer signatures, notes, timesheet submission, barcode scanning, and other completion requirements.

### Impact
- A modernized driver fulfillment flow powered by the new route-based data model while maintaining backward compatibility with systems that still depended on the legacy model.
- Reduced complexity inside the driver app. By moving fulfillment logic toward the new model, the app became easier to maintain and extend, making future product work less constrained by legacy assumptions.
- The migration occurred without disrupting live operations.



## Dots: [Analytics Dashboard](https://www.loom.com/share/35250740c3a54e36a0080be862ea0ebb)
Dots was a YC-backed startup that built software for managing Discord and Slack communities at scale.
 
I worked closely with the CTO to build analytics dashboards that helped customers understand community engagement and growth across their online communities

### Highlights
 - Built analytics dashboards for community managers operating Discord and Slack communities at scale. 
 - Helped customers track engagement, growth, and activity trends across their communities. 
 - Worked directly with technical leadership in a fast-moving early-stage startup environment. 
 
### Impact
 - Helped improve visibility into community health and engagement for Dots customers. 
 - Contributed to customer-facing analytics capabilities during an early stage of the company’s product development.

[Watch a quick video of the dashboard here](https://www.loom.com/share/35250740c3a54e36a0080be862ea0ebb)

<img width="1417" alt="Screen Shot 2022-04-10 at 19 26 00" src="https://user-images.githubusercontent.com/13739454/198871787-12aaa2b9-e381-4320-bd77-a7576e8649c4.png">
<img width="1429" alt="Screen Shot 2022-04-10 at 19 19 17" src="https://user-images.githubusercontent.com/13739454/198871793-859beba0-02b0-49c2-9113-30f8c8187eb8.png">




