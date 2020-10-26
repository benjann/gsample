# gsample
Stata module for random sampling

`gsample` draws a random sample from the data in memory. Simple random sampling
(SRS) is supported, as well as unequal probability sampling (UPS), of which
sampling with probabilities proportional to size (PPS) is a special case. Both
methods, SRS and UPS/PPS, provide sampling with replacement and sampling
without replacement. Stratified sampling and cluster sampling is also
supported.

To install `gsample` from the SSC Archive, type

    . ssc install gsample, replace

in Stata. Stata version 9.2 or newer is required. Furthermore, the `moremata` 
package is required. To install `moremata` from the SSC Archive, type

    . ssc install moremata, replace

---

Installation from GitHub:

    . net install gsample, replace from(https://raw.githubusercontent.com/benjann/gsample/main/)
    . net install moremata, replace from(https://raw.githubusercontent.com/benjann/moremata/master/)

---

Main changes:

    25oct2020 (version 1.0.8)
    - new -rround- option for random-rounding of sample sized across strata
    - new -nopreserve- option to avoid restoring data in case of error or Break; not
      relevant if -generate()- is specified
    - changed approach to preserve data (not relevant if -generate()- is specified);
      earlier versions used -nobreak- and -capture- to make sure that the data will
      be preserved on error, but this meant that the user could not stop -gsample-
      once it was running; this is fixed

    23oct2020 (version 1.0.7)
    - released on GitHub
    - gsample could break if a noninteger sample size was specified; this is fixed;
      noninteger sample sizes will now be rounded to the closest integer
    - new -alt- option to chose a faster SRSWOR algorithm
    - new -nowarn- option to draw an UPSWOR sample even if the conditions for
      unbiased sampling are violated

    06apr2006
    - first released on SSC

