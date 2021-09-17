## GaussianExample_2D.ipynb
Example to use the OmniFold algorithm to do unfolding in 2D. Modified from the 1D example of https://github.com/hep-lbdl/OmniFold

## Root files
The root files neut_flattree.root and genie_flattree.root contain the MC events produced by the NEUT and GENIE generators respectively, after full MC simulation and event reconstruction in the ND280 detector.

Variable type:

    I: integer
    F: float

TTree:

    selectedEvents: reconstructed events
    - dptt_rec/F, dptt_truth/F, pN_rec/F, pN_truth/F, daT_rec/F, daT_truth/F: reconstructed and true TKI variables
    - cutBranch/I: 0 = signal sample, 1 = CC1pi+1pi- enriched sample, 2 = CC1pi+Xpi0 enriched sample, 3 = CC-other-Xpi0 enriched sample, 4 = CC-other-0pi0 enriched sample
    - topology/I: 0 = CC0pi, 1 = CC1pi+0p, 2 = CC1pi+1p, 3 = CC1pi+Np, 5 = CC1pi+1pi-, 6 = CC1pi+Xpi0, 7 = CC-other-Xpi0", 8 = CC-other-0pi0, 9 = background, 10 = OOFV, 11 = OOPS
    - target/I: 1 = H, 6 = C, 8 = O, 13 = Al, 26 = Fe, 29 = Cu, 30 = Zn, 82 = Pb, 999 = other
    - muMomRec/F, muMomTrue/F, muCosThetaRec/F, muCosThetaTrue/F, pMomRec/F, pMomTrue/F, pCosThetaRec/F, pCosThetaTrue/F, piMomRec/F, piMomTrue/F, piCosThetaRec/F, piCosThetaTrue/F: reconstructed and true momentum and angle of the highest momentum muon, proton and proton
    - Enutrue/F: true neutrino energy
    - weight/F: event weight

    trueEvents: all events happening in FGD1 FV
    - dptt_truth/F, pN_truth/F, daT_truth/F: true TKI variables
    - topology/I: 0 = CC0pi, 1 = CC1pi+0p, 2 = CC1pi+1p, 3 = CC1pi+Np, 5 = CC1pi+1pi-, 6 = CC1pi+Xpi0, 7 = CC-other-Xpi0", 8 = CC-other-0pi0, 9 = background, 10 = OOFV, 11 = OOPS
    - target/I: 1 = H, 6 = C, 8 = O, 13 = Al, 26 = Fe, 29 = Cu, 30 = Zn, 82 = Pb, 999 = other
    - muMomTrue/F, muCosThetaTrue/F, pMomTrue/F, pCosThetaTrue/F, piMomTrue/F, piCosThetaTrue/F: true momentum and angle of the highest momentum muon, proton and proton
    - Enutrue/F: true neutrino energy
    - weight/F: event weight
    
## Plot_TKI.ipynb
Example to plot the TKI variables inside the root files, using the python uproot module

## TKI_OmniFold.ipynb
Working but obviously not optimal example to unfold the TKI variables
