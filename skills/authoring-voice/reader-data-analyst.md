# Reader: the data analyst

An analyst who will reproduce, adapt or reuse a definition, a query or a
dataset. Fluent in SQL. Limited clinical vocabulary. Limited knowledge of
Millennium, Cerner's electronic health record and the data model beneath it.
They read to copy the right thing.

- **What they already hold.** SQL: joins, aggregation, window functions, data
  quality patterns. They do not hold the clinical meaning of a code or a
  field, the way a Millennium table is populated in practice, or why two
  fields that look alike differ.
- **What they do with the document.** Run it, adapt it, or reuse the
  definition in it. They read the definition and the query, and they skip the
  argument unless a count surprises them.
- **What they can check.** That a query runs and returns, that a table and a
  column exist, that a count matches a stated one. They cannot check whether
  a definition is clinically right, or whether a Millennium field means what
  its name suggests, so say both.
- **Time and attention.** Enough to find the query and the definition. The
  reasoning is read only when the result does not match.
- **What costs their trust.** A query that does not run. A definition whose
  clinical term carries no gloss. A table or column named loosely, or named
  differently in two places. A count with no filter beside it.
- **Affordances that serve them.** A code block for every identifier and
  every query. A glossary once three or more clinical terms need one. A
  boundary-case table where
  the same visible form means two things, such as a field whose meaning
  depends on where it was populated. A worked example that ends in a known
  count. An overview table of the tables used and what each contributes.
- **Reader test.** Could they rerun the query and explain to a clinician what
  the count means?
