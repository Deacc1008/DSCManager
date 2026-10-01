# DSC Management – Clients with No DSC

This version implements the requested flow:

1. **List of Clients with No DSC**
2. Multiple authorised signatories per client are supported.
3. If two authorised signatories do not have DSCs, both names appear under the same client.
4. If only one signatory is missing a DSC, only that signatory is displayed and the row has **Add DSC**.
5. The client list remains the main view.
6. Clicking a client opens the client detail view, including the existing DSC summary cards.
7. The fetched authorised signatories are displayed in the client detail view with:
   - Name
   - Designation
   - PAN
   - Source portal
   - DSC Available / DSC Not Available
   - Add DSC action for missing DSCs
8. Existing DSC certificates are shown separately in the DSC Management section.

## API integration
The mock uses JavaScript data in the `clients` array.

Replace that data with the API response:
- `authorisedSignatories` = portal/API response
- `dscs` = DSC Management response

The UI automatically calculates the missing DSC list by comparing `dscPresent` / DSC records.

Upload `index.html` to the root of a GitHub Pages repository.
