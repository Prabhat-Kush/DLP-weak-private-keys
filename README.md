# DLP_weak_keys
Methods to detect weak or vulnerable private keys in various Elliptic Curve standards.

Basic Description about codes:

1) Source Files:

There are three source files which are widely used to run the scripts - 
- setup_methods.py,
- implicit_bsgs.py, 
-implicit_kangaroo.py

These have all the necessary functions needed to run various scripts.

Note: If one encounters errors related to print function in setup_methods.py, it's mostly because default might be python2, not python3. To overcome that, one can use print function of python3 in python2 by including "from __future__ import print_function" as the very start of script "setup_methods.py"


2) Counting weak keys in various curves:
We have divided the various curve standards into a few categories. Mainly,

GetStats-112.sage : Curves providing security below 128 bits 

GetStats-128.sage : Curves providing security between 128 and 192 bits

GetStats-192.sage : Curves providing security between 192 and 256 bits

GetStats-256.sage : Curves providing security at least 256 bits

GetStats-Updated-pairing-128.sage : Updated pairing friendly curves providing 128-bit security

GetStats-Updated-pairing-192.sage : Updated pairing friendly curves providing 192-bit security

GetStats-Updated-pairing-256.sage : Updated pairing friendly curves providing 256-bit security


To get the data for various standards for each category, one should run that particular script. 

3) Certicom Challenge Curves:
There are 14 scripts, one each for 14 Certicom Challenge Curves. Out of these 14 Certicom scripts, 

- 5 are for over prime fields (ECCp_131.sage, ECCp_163.sage, ECCp_191.sage, ECCp_239.sage, ECCp_359.sage), 
- 5 are for binary curves (ECC2_131.sage, ECC2_163.sage, ECC2_191.sage, ECC2_238.sage, ECC2_353.sage), and 
- the remaining 4 are for Koblitz curves  (ECC2K_130.sage, ECC2K_163.sage, ECC2K_238.sage, ECC2K_358.sage). We can run any of curve script to check that while we find the solution for randomly generated (weak) DLP instance but the given Certicom challenge DLP instance is not solvable, which shows that the private key given in the Certicom challenge DLP instance is not weak, subject to certain bounds.
