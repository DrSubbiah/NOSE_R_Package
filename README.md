# NOSE_R_Package


# nose: Classification of Sparseness in 2×2 Categorical Data

[![CRAN version](https://www.r-pkg.org/badges/version/nose)](https://cran.r-project.org/package=nose)

[![CRAN Downloads](https://cranlogs.r-pkg.org/badges/nose)](https://cran.r-project.org/package=nose)

[![License: GPL-2](https://img.shields.io/badge/license-GPL%20\(2\)-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html)

---

## Overview

**nose** provides functions for classifying sparseness in 2×2 categorical data where one or more cells have zero counts. It uses three widely applied summary measures:

* **Risk Difference (RD)**
* **Relative Risk (RR)**
* **Odds Ratio (OR)**

The package helps in selecting suitable continuity corrections for zero cells in multi-centre or meta-analysis studies.

Reference: Subbiah and Srinivasan (2008), *Statistics and Probability Letters*, [doi:10.1016/j.spl.2008.06.023](https://doi.org/10.1016/j.spl.2008.06.023)

---

## Installation

```r
install.packages("nose")
```

---
```{r}
# Load package
library(nose)

# Example two 2x2 table with zero cells
x <- matrix(c(0, 10, 5, 15,0, 0, 2, 25), nrow = 2,ncol=4)

# Compute Risk Difference
rd_result <- nose.rd(x,0.01)
print(rd_result)

# Compute Relative Risk
rr_result <- nose.rr(x,0.01)
print(rr_result)

# Compute Odds Ratio
or_result <- nose.or(x,0.01)
print(or_result)
```
## Documentation

* CRAN page: [https://cran.r-project.org/package=nose](https://cran.r-project.org/package/nose)
* Reference manual: [nose.pdf](https://cran.r-project.org/web/packages/nose/nose.pdf)

---

## Citation

```
Subbiah, M. (2025). nose: Classification of Sparseness in 2-by-2 Categorical Data.
R package version 1.0.5. https://CRAN.R-project.org/package=nose
```

---

## License

**nose** is licensed under **GPL-2**.

---


