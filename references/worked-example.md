# Worked example: a file-transfer product

This is a fictional example, not a research report or shipped product. It demonstrates decisions that transfer to another domain. Search terms below are hypotheses; no search volumes, rankings, traffic or conversions have been measured.

## Product and first tool

RelayBox helps freelance video editors send large files to clients. A useful adjacent task is estimating an upload's duration from file size and upload speed. Someone can complete that task without signing up. A relevant next step is learning how to send the file and share its link; avoid promising that this product increases the user's network speed.

Candidate hypotheses to investigate:

| Tool                      | Possible query             | Why it might help                                             | What still needs evidence                                           |
| ------------------------- | -------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------------- |
| Upload-time estimator     | upload time calculator     | Explains whether a client delivery will take minutes or hours | Current results, intent, unmet needs and demand                     |
| Video-file-size estimator | video file size calculator | Helps budget upload size before encoding                      | Whether this audience needs it and how current tools handle bitrate |
| Transfer-speed converter  | Mbps to MB/s               | Resolves confusing network/file units                         | Whether a separate page adds value over the estimator's explanation |

Choose the upload-time estimator for an illustrative pilot, not because the table establishes a ranking opportunity.

## A method that can be independently checked

Use decimal file units explicitly: 1 GB = 1,000,000,000 bytes, 1 MB = 1,000,000 bytes. Network Mbps means 1,000,000 bits per second. If binary units are offered, label GiB and MiB separately.

`ideal seconds = file bytes × 8 / (upload Mbps × 1,000,000)`

At 100 Mbps, 1 decimal GB takes 80 seconds in an ideal transfer. At 20 Mbps it takes 400 seconds, or 6 minutes 40 seconds. If a deliberately chosen efficiency of 80% is offered, divide the ideal duration by 0.8: the latter example becomes 500 seconds, or 8 minutes 20 seconds. Label that assumption; neither outcome guarantees real transfer time. A congestion, protocol-overhead or speed variation range needs a source or an explicit user-configurable assumption.

Keep full precision for computation and round only the display. Choose an explicit display convention for very small nonzero durations. Zero file size may produce zero; upload speed must be finite and positive. Reject blank, negative and non-finite input without retaining a previous result. Test GB versus GiB if both are supported, and check display carry at minute/hour boundaries.

## One complete page

Suggested path: `/tools/upload-time-calculator/`, adapted to the host's routing convention. Use the configured production origin for a self-canonical, not RelayBox's fictional name. Include the estimator, unit explanation, worked example, limitations and a relevant product link. Link it from the existing tools hub and include its canonical path in the sitemap if intended for indexing.

## Expand by usefulness

- A video-size calculator can justify a separate task: bitrate and duration determine file size. Resolution alone does not. Different formats or frame sizes are not enough to infer file size without additional assumptions.
- A download-time calculation may share the same engine. Check search intent and user value before choosing a separate route; it can remain a mode.
- Pages for every file size or city repeat the same calculation without new rules. Use presets on the main tool unless real evidence supports a distinct useful page.

## Proof and measurement

An implementation can prove arithmetic, input handling, visible explanations, metadata and link integration locally. It cannot prove organic demand, indexing or future traffic from this example. A later live pilot would separate impressions, search clicks, completed calculations and relevant conversions. Keep raw file names and typed values out of analytics payloads.
