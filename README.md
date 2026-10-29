# Hi, I'm Adejumoke

I'm building **Medshield**, a healthcare web application that helps people understand medical information and find their next step in care.

## Why I'm building it

Receiving a medical report can leave someone with more questions than answers. Understanding the wording is one challenge; knowing where to book an appointment, speak with a specialist or find a pharmacy is another. Medshield brings these related needs into one application.

## The three parts of Medshield

### Medshield Clear — understand a written report

The goal is to turn the written text in lab reports, imaging reports and discharge summaries into educational plain-language explanations. Users review extracted text before analysis. This is about explaining report wording, not diagnosing a patient or interpreting medical images.

I'm researching a locally hosted model so this feature does not depend on paid chat API calls for each explanation. Training and evaluation have been implemented, but the current model has not passed its development quality gate and does not reliably complete full reports within one minute. Public medical analysis remains disabled while that work continues.

### Medshield Check — look up a medicine code

Patients can enter or scan a medicine code, or check codes in a batch, against a configured dataset. The application includes catalogue administration and concern reporting. A dataset match is not proof that a medicine is genuine; an unknown code is not proof that it is counterfeit. Official registration data still requires an authorized, current source.

### Access healthcare — find the next step in care

The interface has three routes:

- **Hospital appointments:** find hospitals near a chosen area and compare available public ratings before contacting a hospital.
- **1:1 consultations:** choose virtual or physical care and enter the type of consultant you want to see.
- **Pharmacies:** prepare an existing prescription and look for nearby pharmacies, with delivery enquiries or walk-in collection preferences.

The pages are implemented. Live listings need configuration, and confirmed bookings, consultations, stock and delivery need verified provider connections. Medshield does not currently process those arrangements.

## What exists today

The application includes report text extraction and review, medicine dataset workflows, care discovery pages, account and history functionality, and a local ML research pipeline. The engineering work uses Next.js, React, TypeScript, Supabase and Python. It includes validation, privacy boundaries and tests; those software checks do not establish clinical accuracy or a live service.

Prescription text in the care-discovery form stays in page memory. It is not saved or sent to the model, Google or a pharmacy by that feature. Location sharing for provider discovery is an explicit user choice.

## What comes next

1. Improve local report simplification with representative, authorized, clinician-reviewed report data and fresh evaluation.
2. Meet the response-time target while preserving findings, numbers, negation and uncertainty.
3. Connect verified hospitals, consultants and pharmacies for actual availability, booking and fulfilment.
4. Complete live integration and release checks before public use.

**Status: in development and research.** Medshield is not a clinically validated service, does not diagnose or prescribe, and does not claim regulator affiliation.

The source code and trained model are maintained in a private repository. This profile shares the product vision and honest progress without publishing the implementation.
