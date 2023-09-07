
# Provably Unlinkable Smart Card-based Payments
## by Sergiu Bursuc, Ross Horne, Sjouke Mauw, and Semen Yurkov (CCS2023)

The file ```UTX-security.pv``` contains the code specifying the injective agreement and secrecy properties for UTX. 

The files ```compromised/UTX_noVerh.pv``` and ```compromised/UTX_chi-compromised.pv``` represent the scenarios from the end of Section 4.4.

 ```UTXL``` directory contains the files verifying low-value contactless payment in case the PIN is exposed (Appendix C of the extended version available [here](https://arxiv.org/abs/2309.03128).

```tools-testing``` directory contains privacy models. 

All models were verified on 2018 MacBook Pro with 2,6 GHz 6-Core Intel Core i7 and 16 GB of RAM under macOS Ventura 13.5.1. The respective time it takes for the model to terminate is given at the beginning of each .pv file. 
