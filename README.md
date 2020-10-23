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

    . net install reldist, replace from(https://raw.githubusercontent.com/benjann/gsample/master/)
    . net install moremata, replace from(https://raw.githubusercontent.com/benjann/moremata/master/)

---

Main changes:

    23oct2020 (version 1.0.7)
    - released on GitHub
    - gsample could break if a noninteger sample size was specified; this is fixed;
      noninteger sample sizes will now be rounded to the closest integer
    - new -alt- option to chose a faster SRSWOR algorithm
    - new -nowarn- option to draw an UPSWOR sample even if the conditions for
      unbiased sampling are violated

    06apr2006
    - first released on SSC

