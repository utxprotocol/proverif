Models in this folder support our case study described in Section 4.4. of the extended version of the paper *Provably Unlinkable Smart Card-based Payments* (CCS2023) by Sergiu Bursuc, Ross Horne, Sjouke Mauw, and Semen Yurkov available [here](https://arxiv.org/abs/2309.03128). The study investigates whether state-of-the-art tools can be used confidently to prove the unlinkability of UTX and involves the full UTX protocol and the related, strictly simpler, key agreement phase defined in earlier work. 

The verification results are presented in the table below, where `¯\_(ツ)_/¯` stands for the cannot be proved verdict and :heavy_check_mark: and :x: indicate whether the verdict is correct or not, given that the correct results for the protocols tested are known from the related work *Unlinkability of an Improved Key Agreement Protocol for EMV 2nd Gen Payments* by Ross Horne, Sjouke Mauw, and Semen Yurkov and available [here](https://doi.org/10.1109/CSF54842.2022.9919666). 

- T1 models are the outputs of the tool described in *Proving Unlinkability using ProVerif through Desynchronised Bi-Processes* (CSF2023) by David Baelde, Alexandre Debant and Stéphanie Delaune available [here](https://hal.science/hal-03674979/). They must be processed by the plain ProVerif, as well as PV models.
- T2 models should be processed by the tool described in *Indistinguishability Beyond Diff-Equivalence* (CSF2023) by Vincent Cheval and Itsaka Rakotonirina available [here](https://www.dropbox.com/sh/t0bwuppbjab0dka/AADFc5E-zDlLPMyvF80fa1Sua?dl=0).
- The model `UTX-privacy_PV_diff.pv` was kindly provided by the reviewers of the paper in an attempt to express the unlinkability of UTX as a diff-equivalence problem. This model runs forever, similarly to other `UTX-privacy` models.

|                |PV 2.04 diff                   |T1 diff              |T2 obs |
|----------------|--------------------------|------------------------- |-------
|BDH (no T)      |`¯\_(ツ)_/¯ `             |`TRUE`    :x:             | `¯\_(ツ)_/¯`
|BDH (full)      |`running forever`         |`TRUE`          :x:       | `¯\_(ツ)_/¯`
|UBDH (no T)     |`TRUE` :heavy_check_mark: |`TRUE` :heavy_check_mark: | `TRUE` :heavy_check_mark:
|UBDH (full)     |`running forever`         |`TRUE`  :heavy_check_mark:| `TRUE`:heavy_check_mark:
|UTX.            |`running forever`|        `fatal error`              | `running forever`

Please consult Section 4.4. of [the paper](https://arxiv.org/abs/2309.03128) for details.  