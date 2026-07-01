# 16. Search (Threat Hunting)

_Part: Hunt & Intelligence_

Proactively look for suspicious activity across all endpoints.

**Path:** `XDR Threat Investigation ▸ Search`

1. Select a **data source** (e.g., Endpoint Activity Data).
2. Build a query with field filters, for example:
   - Encoded PowerShell: `processCmd:*EncodedCommand*`
   - LOLBins: `processName:(mshta.exe OR wscript.exe OR rundll32.exe)`
3. Adjust the **time range** and run the search.
4. Click a result to pivot into detail, or **Save** the query for reuse.

**Tip:** From Workbench, right-click an entity and choose **Search** to pivot instantly.

---

[← Previous: Response Management](../15-response-management/) · [Index](../) · [Next: Custom Detections & Watchlists →](../17-custom-detections-watchlists/)
