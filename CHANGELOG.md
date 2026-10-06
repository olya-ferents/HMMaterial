## v1.0 — baseline audit
Known defects: contradiction on fee disclosure, unverifiable tone requirement, no instruction for missing-data case.

Not measured: frequency of occurrence.

## v1.1 — requirements clarification

Version: v1.1
Owner: Not specified
Reviewer: Not specified

Changed:
- Replaced the general empathy requirement with a testable rule requiring the
  first sentence to acknowledge a lost or stolen card before giving procedural
  instructions.
- Defined "recent transactions" as transactions from the last 30 calendar days
  when the customer does not specify another period.
- Added a rule to retrieve transactions for a customer-specified period when
  one is provided.
- Replaced the product-account edge case with a source-grounded rule requiring
  `search_knowledge_base` before answering.
- Prohibited inventing product terms, rates, deposits, withdrawal conditions,
  or other details when the search result is empty or lacks the requested
  information.

Evidence:
- `base.v1.1.md` section 1 defines the acknowledgement behavior.
- `base.v1.1.md` section 4 defines the transaction time window and retrieval
  behavior.
- `base.v1.1.md` section 6 requires knowledge-base retrieval and prohibits
  inferred product details.