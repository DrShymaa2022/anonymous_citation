This folder contains files needed for Africa Crypt 2026 Submitted manuscripts (by the same author but anonymized), mainly:

1- All cited posters with author name removed

2- The extended version of the paper about Estonia i-voting system, and also some figures in PDF format.

3- the last version of the automated formal verification (using PRoVerif2.05) of the court verifiability e-voting paper:
The paper states that this part is still WIP, so:

(**court.pv**) contains the version at submission time, 

(**court_final.pv**) contains the most updated version
            
(**runresult.txt**) contains the details of the last run (of the updated version)

On 25/3/2026:

The code successfuly checks the predicates measuring the following: (all true)

    Judge_accepts
    Judge_rejects_voterclaim
    Judge_falsfies_election
    coercer_deceived
    auditor_accepts

On 28/3/2026:

a) axioms are added to represent ZKPs in summary reports.

b) checking ZKP is successfully added to the auditor_accepts query.

c) The code successfuly checks a new predicate about absent voting: (all true)

            judge_rejects_absentvoting_claim

On 29/3/2026:

a) added an authentication function to make it accurately reflect the true system (there is identity and auth_id)

b) removed unnecessary parameter (bool) from the check of non-inclusion, replacing it by  comparing to h_NULL value (instead of returning true/false, the ZKP whatever it is returns either the corresponding HBID if it exits, or a designated h_NULL if not)

c) The code successfuly runs (all true ) with adding a new predicate about when to accept absent voting claim:

            judge_accepts_absentvoting_claim

On 30/3/2026:

just a little refinement that both absent voting queries (whether accept or reject the voter claim) take the bitstring identity (i.e. not the biometric authenticated identity) because voter claims not being there at all (no HBID, no receipts, no biometric check ... just submitting his/her identity card)
