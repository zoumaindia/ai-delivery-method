# DECISIONS

Use this file to capture durable rationale for non-obvious choices.

## Example entry

### Choose server-side PDF generation for contract exports (YYYY-MM-DD)

**Decision:**  
Use a server-side PDF path for canonical exports.

**Why:**  
The document must be consistent across environments and printable outside the browser.

**Implication:**  
Deployment/runtime dependencies must be part of release verification.
