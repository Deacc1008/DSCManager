# DSC Management – Combined UI V8

Single-screen design with two side-by-side areas:

## All DSC
Large left panel containing:
- Every DSC currently available in DSC Management
- Every fetched GST/TDS/ITR Authorised Signatory
- Portal-specific signatory rows
- DSC Available / DSC Not Available status
- Matched DSC details
- Unmatched DSCs already in DSC Management
- Add DSC action for missing signatories
- Search and filters
- Export

## Clients with No DSC
Smaller right panel containing only customers with at least one portal signatory whose DSC is missing.

Each client is grouped and shows:
- Portal
- Signatory
- PAN
- Designation
- Add DSC

## Client Details
Click a client to see:
- Client identifiers
- DSC/signatory summary
- GST/TDS/ITR signatories
- Which signatories have DSC
- Which signatories need DSC
- All DSCs available for the client
- DSCs that cannot be matched to a portal signatory

## Demo scenarios
The dummy data includes:
1. Multiple signatories under one portal.
2. Different signatories for GST, TDS and ITR for the same client.
3. A customer having DSCs not present in the portal signatory response.
4. A mixed case where GST and ITR have DSCs but TDS does not.
5. Add DSC flow from a missing signatory row.

The UI is a prototype. Replace the in-memory arrays and save function with production APIs/database services.
