## Proposal

That org adopt an annual process of support a new version of R and remove support for an old version of R.

That org support 2 versions of R concurrently - the first patch of each of 2 most recent  minor releases ( e.g. 4.2.1 and 4.1.1)

## Actions

Annually, following the release of the first patch for the latest version of R - test all existing projects, products developed with that year's retiring version for compatibility with patch 1 of the latest  release.

This would typically be in a window of several months between June (depending on the timing of the release by the R Core team) and the end of October.

Annually, in November, retire the oldest supported version of R at org and install the first released patch of the latest minor release.

From November new projects/products are to be developed in the org's current R version.

Develop a register of products/projects and workflows that need to be tested and a framework for testing.

### Proposed release support schedule

|  Date |Current R version   |Previous R Version   |  Retired R version |
| ------------ | ------------ | ------------ | ------------ |
| November 2021  | 4.1.1   | 4.0.1  | 3.6.1  |
| November 2022  |  4.2.1 |  4.1.1 | 4.0.1  |
| November 2023  | 4.3.1   | 4.2.1  |  4.1.1 |
| November 2024  |  4.4.1 |  4.3.1 | 4.2.1  |

## Desired Outcomes

Standardisation of R versions used across org.

Only support versions of R for which Windows binaries are available for CRAN packages - this is a better user experience for less experienced R users. It also does not require additional tooling installed on Windows for building packages from source (some users will require the additional tooling regardless).

Assists IT in supporting and maintaining packages for the installation of R and R packages from CRAN.

Avoids reproducibility problems between teams and projects by keeping the range of R versions to a narrow and up to date range.

Avoids 'fear of upgrade' by enforcing bi-annual checking/testing of projects/products for compatibility with latest releases.

Give users access to latest improvement, features and bug fixes.

## Background

Org uses the Windows operating system.

Define a strategy for which releases or the [R software environment for statistical computing and graphics](https://www.r-project.org/ "R software environment for statistical computing and graphics") are maintained and supported at org.

### R release versioning and timing

The R Core team uses semantic versioning for R releases.

The format is R x.y.z where:

x is the major version (infrequent, on average once every 5 years)
y is the minor version (annually, between March and May)
z is the patch version (one or more patches for each minor release. Patch 1 typically released between June and August)

### Past 12 releases April 2020 to June 2022
| Version | Release month | Release Year | Type  |
| ------- | ------------- | ------------ | ----- |
| R 4.2.1 | June          |  2022        | Patch |
| R 4.2.0 | April         |  2022        | Minor |
| R 4.1.3 | March         |  2022        | Patch |
| R 4.1.2 | November      |  2021        | Patch |
| R 4.1.1 | August        |  2021        | Patch |
| R 4.1.0 | May           |  2021        | Minor |
| R 4.0.5 | March         |  2021        | Patch |
| R 4.0.4 | February      |  2021        | Patch |
| R 4.0.3 | October       |  2020        | Patch |
| R 4.0.2 | June          |  2020        | Patch |
| R 4.0.1 | June          |  2020        | Patch |
| R 4.0.0 | April         |  2020        | Major |


[Previous releases of R for Windows](https://cran.r-project.org/bin/windows/base/old/ "Previous releases of R for Windows")

### Availability of cran package binaries for Windows

Packages for R 4.x are built (if possible) whilst 4.(x+1) is current, but building stops once 4.(x+2) reaches alpha (pre-release, about a month before release).

e.g. Binaries available for R 4.0 from release in April 2020 until a month before R 4.2  was released in March 2022   

The CRAN policy is to archive binary packages two years after the 3.x or 4.x series is closed. 

On Windows from source rather than a binary can lead to longer package install time for packages that have native code/DLLs and require RTools be installed.

https://cran.r-project.org/bin/windows/base/rw-FAQ.html#No-binary-packages-appear-to-be-available-for-my-version-of-R

check here for definitive lists of R series package binary support

https://cran.r-project.org/bin/windows/contrib/ReadMe



| R 'Series' | End of CRAN package binaries |
| ---------- | ---------------------------- |
| 3.6        | April 2021                    |
| 4          | March/April 2022             |
| 4.1        | March/April 2023             |
| 4.2        | March/April 2024             |


### Differences between minor versions

Each release has a NEWS file attached documenting changes.
[History of all NEWS files can be viewed here ](https://cran.r-project.org/doc/manuals/r-release/NEWS.html "History of all NEWS files can be viewed here ")

[Installed packages with native code/DLLS are incompatible between minor versions e.g. 4.1 to 4.2](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#What_0027s-the-best-way-to-upgrade_003f "Installed packages with native code/DLLS are incompatible between minor versions e.g. 4.1 to 4.2")

### Upgrading packages between R versions
[Official advice ](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#What_0027s-the-best-way-to-upgrade_003f "Official advice ")

### Links

[CRAN R for Windows FAQ](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#Introduction "CRAN R for Windows FAQ")

[Updated CRAN packages RSS feed](https://dirk.eddelbuettel.com/cranberries/cran/updated/ "Updated CRAN packages RSS feed")
