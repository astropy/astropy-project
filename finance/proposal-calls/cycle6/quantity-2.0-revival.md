### Reviving, completing and unblocking Quantity 2.0

**Proposal Category**: Innovations

### Project Team
- Marten van Kerkwijk (@mhvk)
- Clément Robert (@neutrinoceros)
- Nathaniel Starkman (@nstarman) **TBC**

### Project Description / Scope of Work
We plan to revive, complete and lift the existing blocking issues within the
currently stalled Quantity 2.0 project, which aligns with the top item on the
community-defined priority list.

#### High Priority Objectives
O1:
- KR1.1
- KR1.2

#### Project / Work / Deliverables

There are two high levels goals to this work. We expect them to take roughly the
same amount of effort and to tackle them sequentially
1. getting the project as it exists to the finish line. This means:
   - completing implementation
   - completing test coverage
   - making strict Array API compatibility checks pass (already mostly done)
2. lifting the most significant limitation, i.e. that erfa routines are ufuncs
  and not compatible with the Array API. Defining the correct solution to this
  problem is very much part of the work that needs to be done so we don't have
  a detailled plan for it yet, though we have a couple ideas we'd like to
  explore, which the funding we're requesting will allow us to do.

@mhvk is to serve as the principal investigator, and will be primarily focused,
as a developer, on the first phase. Later on, we expect his role to switch to
consulting.

@neutrinoceros will be the first interlocutor and main reviewer over the first
phase, and provide the bulk of the work force over the second one.

Secondary goals include:
- invest time in performance tailoring, as we know that Quantity 2.0 is
  currently measurably slower than `astropy.units`. We do want to avoid
  pre-mature optimization and we expect a performance cost to restricting the
  code to the Array API anyway, so this is not a high priority. 
- `astropy.utils.masked` and `astropy.uncertainty` could in principle follow a
  similar path in the future and move towards strict Array API compliance, so
  we'd like to provide guidelines and pave the road for this effort if we find
  sufficient similarities.


### Approximate Budget
Currency: US $

- Salary / contractor fee: $52,000
  breakdown:
    - Marten requests for 200hrs at $150/hr ($30,000) 
    - Clement requests for 200hrs at $110/hr ($22,000)
- TOTAL: $52,000

Please note that we would happily accept budget items other than the above.

### Period of Performance

Jan 1, 2027–Dec 31, 2027
