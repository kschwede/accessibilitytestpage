# Broken Links Audit

Audit time: 2026-03-26 21:45 UTC

Scope: generated site in `/tmp/accessibilitytestpage_build`, corresponding to the published GitHub Pages project at `https://kschwede.github.io/accessibilitytestpage/`.

## Summary

- Confirmed local broken links: 16
- Deployment-path issues on the GitHub Pages project URL: 1 unique target paths
- Confirmed external broken links: 7
- External links with indeterminate status (for example 403/429): 29

## Confirmed Local Broken Links

| Source file | Element | URL | Problem |
| --- | --- | --- | --- |
| `m661011.html` | `a[href]` | `hw1661011.pdf` | missing target file |
| `m661011.html` | `a[href]` | `hw2661011.pdf` | missing target file |
| `m661011.html` | `a[href]` | `hw3661011.pdf` | missing target file |
| `m661011.html` | `a[href]` | `hw4661011.pdf` | missing target file |
| `m661011.html` | `a[href]` | `hw5661011.pdf` | missing target file |
| `m6620.html` | `a[href]` | `hw16620.pdf` | missing target file |
| `m6620.html` | `a[href]` | `hw26620.pdf` | missing target file |
| `m6620.html` | `a[href]` | `hw26620bonus.pdf` | missing target file |
| `m6620.html` | `a[href]` | `hw36620.pdf` | missing target file |
| `m6620.html` | `a[href]` | `hw46620.pdf` | missing target file |
| `m6620.html` | `a[href]` | `hw56620.pdf` | missing target file |
| `m662017.html` | `a[href]` | `hw1662017.pdf` | missing target file |
| `m662017.html` | `a[href]` | `hw2662017.pdf` | missing target file |
| `m662017.html` | `a[href]` | `hw3662017.pdf` | missing target file |
| `m662017.html` | `a[href]` | `hw4662017.pdf` | missing target file |
| `m662017.html` | `a[href]` | `hw5662017.pdf` | missing target file |

## Deployment-Path Issues

These links are emitted as root-absolute paths such as `/assets/...`. Because the site is deployed as a GitHub Pages project under `/accessibilitytestpage/`, these paths resolve outside the project and break on the live site.

| Emitted path | Referenced from | Why it breaks |
| --- | --- | --- |
| `/assets/css/site.css` | `index.html`, `index1.html`, `m131113.html`, `m131114.html`, `m1320-006.html`, `m1320-009.html`, `m4800.html`, `m5440_2018.html`, `m5620.html`, `m5750.html`, `m6610.html`, `m661011.html`, `m661014.html`, `m6610_2018.html`, `m6620.html`, `m662012.html`, `m662015.html`, `m662017.html`, `m662019.html`, `m6630.html`, `m663013.html`, `m6630_2020.html`, `m679012.html`, `m787515.html`, `math4800.html`, `movsat.html`, `publications.html` | Root-absolute URL on a project site; expected prefix `/accessibilitytestpage/` or a relative path. |

## Confirmed External Broken Links

| URL | Sources | Result |
| --- | --- | --- |
| `http://bennioncenter.org/about/events/project-youth.php` | `index.html` | <urlopen error [Errno -5] No address associated with hostname> |
| `http://topo.math.auburn.edu/pub/2Olgas-proceedings/pa125-epshteyn.pdf` | `publications.html` | <urlopen error [Errno -2] Name or service not known> |
| `http://www.cqb.utah.edu/index.html` | `index.html` | <urlopen error [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: certificate has expired (_ssl.c:1000)> |
| `http://www.cscamm.umd.edu/people/faculty/tadmor/pub/PDEs/Tadmor%20BAMS_v49-2012.pdf` | `m663013.html`, `m6630_2020.html`, `m787515.html` | HTTP 404 |
| `http://www.math.cmu.edu/~nw0z/publications/08-CNA-023/023abs/023abs.html` | `publications.html` | HTTP 404 |
| `http://www.math.utah.edu/~pa/math/q1.html` | `m131113.html`, `m131114.html` | HTTP 404 |
| `https://www.linkedin.com/in/gabrielle-legaspi-ms-b35a02155/` | `index.html` | HTTP 404 |

## External Links With Indeterminate Status

These URLs responded in a way that is often caused by bot blocking or rate limiting rather than an actually dead page, so they should be checked in a browser before being treated as broken.

| URL | Sources | Result |
| --- | --- | --- |
| `http://www.math.utah.edu/~albright/1311.html` | `m131113.html` | HTTP 403 |
| `http://www.math.utah.edu/~gfan/currentteaching/1320/` | `m1320-009.html` | HTTP 403 |
| `http://www.math.utah.edu/~han/1311labFall2014/` | `m131114.html` | HTTP 403 |
| `http://www.math.utah.edu/~steffen/m1320-007-008.html` | `m1320-006.html` | HTTP 403 |
| `http://www.mathworks.com/access/helpdesk/help/pdf_doc/matlab/getstart.pdf` | `m4800.html`, `m5620.html`, `m5750.html`, `m6610.html`, `m661011.html`, `m661014.html`, `m6610_2018.html`, `m6620.html`, `m662012.html`, `m662015.html`, `m662017.html`, `m662019.html`, `m6630.html`, `m663013.html`, `m6630_2020.html`, `m787515.html`, `math4800.html` | HTTP 403 |
| `http://www.mathworks.com/access/helpdesk/help/techdoc/matlab.shtml` | `m4800.html`, `m5620.html`, `m5750.html`, `m6610.html`, `m661011.html`, `m661014.html`, `m6610_2018.html`, `m6620.html`, `m662012.html`, `m662015.html`, `m662017.html`, `m662019.html`, `m6630.html`, `m663013.html`, `m6630_2020.html`, `m787515.html`, `math4800.html` | HTTP 403 |
| `http://www.mathworks.com/moler/index_ncm.html` | `m787515.html` | HTTP 403 |
| `http://www.sciencedirect.com/science/article/pii/S0025556408001624` | `publications.html` | HTTP 403 |
| `http://www.sciencedirect.com/science/article/pii/S0168927414000191` | `publications.html` | HTTP 403 |
| `http://www.sciencedirect.com/science/article/pii/S016892741400141X` | `publications.html` | HTTP 403 |
| `http://www.sciencedirect.com/science/article/pii/S0168927415000227` | `publications.html` | HTTP 403 |
| `http://www.sciencedirect.com/science/article/pii/S0168927416301672` | `publications.html` | HTTP 403 |
| `http://www.sciencedirect.com/science/article/pii/S0377042706005279` | `publications.html` | HTTP 403 |
| `https://docs.google.com/forms/d/1T2nVCj238M1gh8iXn5qLBNs3lvX219JcuzFAR6enppQ/viewform` | `m131113.html` | HTTP 401 |
| `https://www.linkedin.com/in/charlotte-b-605036243/` | `index.html` | HTTP 999 |
| `https://www.linkedin.com/in/ejasonalb/` | `index.html` | HTTP 999 |
| `https://www.linkedin.com/in/james-eckstein-1b8a80166/` | `index.html` | HTTP 999 |
| `https://www.linkedin.com/in/kamala-liu-7b8682206` | `index.html` | HTTP 999 |
| `https://www.linkedin.com/in/kyle-robert-steffen-03616a146/` | `index.html` | HTTP 999 |
| `https://www.linkedin.com/in/thuong-nguyen-b1bab9132/` | `index.html` | HTTP 999 |
| `https://www.esaim-m2an.org/articles/m2an/abs/2011/03/m2an08111/m2an08111.html` | `publications.html` | HTTP 403 |
| `https://www.esaim-m2an.org/component/article?access=doi&doi=10.1051/m2an/2024012` | `publications.html` | HTTP 403 |
| `https://www.sciencedirect.com/science/article/abs/pii/S004578252500204X` | `publications.html` | HTTP 403 |
| `https://www.sciencedirect.com/science/article/abs/pii/S0168927406000912` | `publications.html` | HTTP 403 |
| `https://www.sciencedirect.com/science/article/pii/S0021999118304996` | `publications.html` | HTTP 403 |
| `https://www.sciencedirect.com/science/article/pii/S0021999121007968?dgcid=coauthor` | `publications.html` | HTTP 403 |
| `https://www.sciencedirect.com/science/article/pii/S1359645422008539` | `publications.html` | HTTP 403 |
| `https://www.worldscientific.com/doi/10.1142/S021820252250052X` | `publications.html` | HTTP 403 |
| `https://www.worldscientific.com/doi/10.1142/S0219530522400036` | `publications.html` | HTTP 403 |

## Method

- Built the site with Jekyll and audited the generated output rather than only the source files.
- Checked relative internal links against the generated site tree.
- Flagged root-absolute URLs as deployment issues because this site is published as a project site under `/accessibilitytestpage/`.
- Checked external HTTP/HTTPS links with live network requests and recorded confirmed failures separately from uncertain bot-blocked responses.
