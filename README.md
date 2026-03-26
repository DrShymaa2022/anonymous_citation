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
