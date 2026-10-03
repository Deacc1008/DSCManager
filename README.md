# DSC Management UI V9

The menu is **DSC Management**.

The module is one screen with two switchable tabs:

1. **All Clients**
   - Shows all DSC records available in DSC Management.
   - Also shows every GST/TDS/ITR Authorised Signatory fetched from the portals.
   - A signatory with a linked DSC is shown as DSC Available.
   - A signatory without a linked DSC is shown as DSC Not Available with Add DSC.
   - DSCs present in DSC Management but not matched to a portal signatory are also shown.
   - Search, portal, DSC status and certificate status filters are included.

2. **Clients with No DSC**
   - Shows only customers having at least one portal Authorised Signatory without a DSC.
   - Client-wise grouping.
   - Portal, signatory, PAN, designation and Add DSC are shown.
   - Search and portal filters are included.

Clicking a client opens Client Details with GST/TDS/ITR signatories, available DSCs and unmatched DSCs.

The prototype contains dummy data for multiple signatories, different signatories by portal, mixed DSC availability and unmatched DSCs.
