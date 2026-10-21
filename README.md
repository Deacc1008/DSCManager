# DSC Manager V13 — UI-matched prototype

This is a standalone HTML prototype restyled to closely follow the DSC Manager application screenshot supplied for this task.

## Included
- Dark left sidebar with DSC Manager branding, client search, navigation, and the 15 dummy clients.
- Overview with Total, Active, Expiring Soon, and Expired cards, expiry status tabs, and a certificate table.
- Certificate search and combined filters for portal, issuing CA, token make, and token color.
- Client-level filtering by clicking a client in the sidebar, including a panel for that client's portal signatories still missing a DSC.
- Clients with No DSC view retaining the six initially missing-DSC clients and per-signatory Add DSC actions.
- Client and certificate detail modals.
- Manual Add DSC form with optional portal-signatory mapping, token make, and token color.
- Demo Scan DSC autofill and a Review sample certificates flow.
- Added certificates persist in this browser using localStorage.

## Run
Open `index.html` in a modern browser, or upload the folder contents to GitHub Pages. It does not require a build step or external CSS framework.

## Important prototype limitation
The scan/token-review functions use sample data only. This does not read a physical USB token, call GST/TDS/ITR portal APIs, or save to a server/database. Added data persists only in the same browser through localStorage.
