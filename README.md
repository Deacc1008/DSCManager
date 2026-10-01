# DSC Management – Interactive Demo V3

This version is interactive for BRD/demo purposes.

### Demo flow
1. Click **+ Demo Data**.
2. Add a dummy client.
3. Select **Add Signatory to Client**.
4. Add 1 or more authorised signatories.
5. Each new signatory is created with **DSC Not Available** and appears in the missing-DSC list.
6. Click **Add DSC** against a signatory.
7. Click Continue in the Add DSC popup.
8. The demo marks that signatory as having a DSC:
   - it disappears from the missing-DSC list if no other signatory is missing;
   - it remains if another signatory is still missing;
   - the DSC appears in the client's DSC Management section.
9. Click the client name to open the detailed client view and see all fetched signatories, including those with and without DSC.

This is dummy-data behavior only. Replace the JavaScript `clients` array and add DSC callback with the actual APIs when the API contracts are available.


## Multi-portal customer example
The demo now includes **Vertex Business Solutions Pvt. Ltd.** where:
- GST → Arjun Kapoor
- TDS → Meera Kapoor
- ITR → Vikram Shah

All three can be missing a DSC and are shown as separate rows in the main list, with the same client grouped using row spans.

The client detail view groups fetched signatories under:
- GST Portal
- TDS Portal
- Income Tax / ITR Portal

Another example, **Nexus Technologies India Pvt. Ltd.**, demonstrates a mixed state:
- GST → DSC Available
- TDS → DSC Not Available
- ITR → DSC Available

This demonstrates that only the missing TDS signatory appears in the missing-DSC list.


## Unmatched / Unmapped DSC scenario
The demo now supports DSCs that already exist in DSC Management but are not present in the fetched GST/TDS/ITR signatory list.

These are marked with `linked:false` and are shown in:
1. A dedicated **DSCs Available but Not Found in Portal Signatory List** section on the main screen.
2. The client's **Client Details** page under the same heading.

Example:
- Client: Nexus Technologies India Pvt. Ltd.
- GST signatory: Sanjay Rao → DSC Available
- TDS signatory: Kavita Rao → DSC Not Available
- ITR signatory: Rohit Rao → DSC Available
- Extra DSC: Pooja Nair → DSC exists in DSC Management, but not found in the portal signatory response → Unmapped

This lets the user see both sides of the reconciliation:
- Portal signatory without DSC
- DSC available without a matching portal signatory
