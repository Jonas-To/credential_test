---
vct: urn:eu:eudi:eucc:1
background_color: "#1a4f8a"
text_color: "#ffffff"
formats: "sd-jwt", "w3c"
---

# EU Company Certificate (EUCC)

A verifiable credential attesting to the legal existence and registration details of a legal person within the EU, as defined in the EUCC Rulebook.

## Claims

- `legal_person_name` "Legal Name" (string): Official registered name of the legal person [mandatory]
- `legal_person_id` "Legal Person Identifier" (string): Unique identifier of the legal person (e.g. EUID) [mandatory]
- `legal_form_type` "Legal Form" (string): Legal form of the entity (e.g. Aksjeselskap (AS)) [mandatory]
- `registration_member_state` "Registration Member State" (string): Alpha-2 country code of the member state where the entity is registered [mandatory]
- `registered_address` "Registered Address" (object): Official registered address of the legal person [mandatory]
  - `full_address` (string): Full address as a single string [mandatory]
  - `thorough_fare` (string): Street name
  - `locator_designator` (string): House number or locator
  - `post_code` (string): Postal code
  - `post_name` (string): City or locality
  - `admin_unit_level_1` (string): Country code (ISO 3166-1 alpha-2)
  - `admin_unit_level_2` (string): Region or county
- `registration_date` "Registration Date" (date): Date of registration in ISO 8601 YYYY-MM-DD format [mandatory]
- `legal_person_status` "Legal Person Status" (string): Current status of the legal person (e.g. active) [mandatory]
- `legal_person_activity` "Legal Person Activity" (object): Primary business activity [mandatory]
  - `code` (string): Activity code (e.g. NACE)
  - `description` (string): Description of the activity
- `share_capital` "Share Capital" (object): Share capital of the legal person
  - `amount` (string): Amount of share capital
  - `currency` (string): Currency code (ISO 4217)
- `legal_person_duration` "Legal Person Duration" (string): Duration or end date of the legal person if applicable
- `digital_contact_point` "Digital Contact Point" (object): Digital contact information
  - `website` (string): Website URL
  - `email` (string): Email address
- `legal_representative` "Legal Representatives  ties authorised to represent the legal person [mandatory]
  - `full_name` (string): Full name of the natural person representative
  - `date_of_birth` (date): Date of birth of the natural person representative
  - `nationality` (string): Nationality of the natural person representative
  - `name` (string): Name of the legal person representative
  - `id` (string): Identifier of the legal person representative
  - `legal_form_type` (string): Legal form of the legal person representative
  - `signatory_rule` (string): Signatory rule (e.g. alone, jointly)
- `issuing_authority` "Issuing Authority" (string): Name of the authority that issued the EUCC [mandatory] [sd=never]
- `issuing_authority_id` "Issuing Authority ID" (string): Identifier of the issuing authority [mandatory] [sd=never]
- `issuing_country` "Issuing Country" (string): Alpha-2 country code of the issuing authority's country [mandatory] [sd=never]
- `issuing_jurisdiction` "Issuing Jurisdiction" (string): Country subdivision code per ISO 3166-2
- `issuance_date` "Issuance Date" (date): Date when the EUCC was issued in ISO 8601 format [mandatory]
- `authentic_source_id` "Authentic Source ID" (string): Identifier of the authentic source [mandatory] [sd=never]
- `authentic_source_name` "Authentic Source Name" (string): Name of the authentic source [mandatory] [sd=never]
- `attestation_legal_category` "Attestation Legal Category" (string): Legal category; QEAA or PUB-EAA [sd=never]
- `trust_anchor` "Trust Anchor" (string): URL of the machine-readable trust anchor for verifying the EUCC [sd=never]
