# Reader: clinical data decision-makers

Clinicians, data scientists and the data management team jointly approving a
clinical-data design. They need one account of the decision, even though they
bring different technical vocabularies to it.

- **What they already hold.** Clinical result concepts, the analytical
  questions the data must answer, and the risks of losing or misclassifying
  source meaning. Do not assume that every reader holds relational modelling,
  Spark, Parquet, struct or schema vocabulary. Keep an exact term where the
  decision needs it, and gloss it for the reader who does not.
- **What they do with the document.** Decide together whether the proposed
  representation preserves clinical meaning, supports analysis and can be
  managed reliably. Each group tests a different part of the same decision.
- **What they can check.** Clinicians can check the clinical distinctions.
  Data scientists can check whether the representation supports valid queries.
  The data management team can check whether fields, quality rules and
  ownership can be operated. No one reader can check the whole proposal unless
  it makes the links between those concerns visible.
- **Time and attention.** They read once to reach a decision, then return to
  the exact fields and rules during implementation or review. The opening must
  make the recommendation understandable before it asks them to inspect its
  storage mechanism.
- **What costs their trust.** A familiar result made obscure by implementation
  vocabulary. A technical term used before its distinction is visible. A
  simplified model that drops clinically or analytically relevant meaning. A
  field whose purpose one group can understand only by deferring to another.
- **Affordances that serve them.** The smallest familiar result example before
  the mechanism. An essential-terms block of three to six terms between that
  example and the technical commitment. A boundary-case table where similar
  visible forms carry different meanings. A compact field table only when its
  rows remain short enough to scan.
- **Reader test.** Could all three groups explain the recommendation, why
  generic value slots are unsafe, and the difference between visible form,
  meaning and rank before they approve it?
