# (APPENDIX) Appendix {-}

# NEWS {#booknews}

## 0.3.0

* 2019-10-03, include in the approval template that maintainers should include link to the docs.ropensci.org/pkg site (ropensci/dev_guide#191)

* 2019-09-26, add instructions for handling editors to nominate packages for blog posts (ropensci/dev_guide#180)

* 2019-09-26, add chapter on changing package maintainers (ropensci/dev_guide#128) (ropensci/dev_guide#194)

* 2019-09-26, update Slack room to use for editors (ropensci/dev_guide#193)

* 2019-09-11, update instructions in README for rendering the book locally (ropensci/dev_guide#192)

* 2019-08-05, update JOSS submission instructions (ropensci/dev_guide#187)

* 2019-07-22, break "reproducibility" category in policies into component parts. (ropensci/software-review-meta#81)

* 2019-06-18, add link to rOpenSci community call "Security for R" to security chapter.

* 2019-06-17, fix formatting of Appendices B-D in the pdf version of the book (bug report by [`@IndrajeetPatil`](https://github.com/IndrajeetPatil), #179)

* 2019-06-17, add suggestion to use R Markdown hunks approach when the README and the vignette share content. (ropensci/dev_guide#161)

* 2019-06-17, add mention of central building of documentation websites.

* 2019-06-13, add explanations of CRAN checks. (ropensci/dev_guide#177)

* 2019-06-13, add mentions of the `rodev` helper functions where relevant.

* 2019-06-13, add recommendation about using `cat` for `str.*()` methods.  RStudio assumes that `str` uses `cat`, if not when loading an R object the `str` prints to the console in RStudio and doesn't show the correct object structure in the properties. ([`@mattfidler`] (https://github.com/mattfidler/) #178)

* 2019-06-12, add more details about git flow.

* 2019-06-12, remove recommendation about `roxygen2` dev version since the latest stable version has what is needed. ([`@bisaloo`](https://github.com/bisaloo/), #165)

* 2019-06-11, add mention of usethis functions for adding testing or vignette infrastructure in the part about dependencies in the package building guide.

* 2019-06-10, use the new URL for the dev guide, https://devguide.ropensci.org/

* 2019-05-27, add more info about the importance of the repo being recognized as a R package by linguist ([`@bisaloo`](https://github.com/bisaloo/), #172)

* 2019-05-22, update all links eligible to HTTPS and update links to the latest versions of Hadley Wickham and Jenny Bryan's books ([`@bisaloo`](https://github.com/bisaloo/), #167)

* 2019-05-15, add book release guidance for editors. (ropensci/dev_guide#152)

## 0.2.0

* 2019-05-23, add CRAN gotcha: in the Description field of your DESCRIPTION file, enclose URLs in angle brackets.

* 2019-05-13, add more content to the chapter about contributing.

* 2019-05-13, add more precise instructions about blog posts to approval template for editors.

* 2019-05-13, add policies allowing using either `<-` or `=` within a package as long as the whole package is consistent.

* 2019-05-13, add request for people to tell us if they use our standards/checklists when reviewing software elsewhere.

* 2019-04-29, add requirement and advice on testing packages using `devel` and `oldrel` R versions on Travis.

* 2019-04-23, add a sentence about why being generous with attributions and more info about ctb vs aut.

* 2019-04-23, add link to Daniel Nüst's notes about migration from XML to xml2.

* 2019-04-22, add use of rOpenSci forum to maintenance section.

* 2019-04-22, ask reviewer for consent to be added to DESCRIPTION in review template.

* 2019-04-22, use a darker blue for links (feedback by [`@kwstat
`](https://github.com/kwstat), #138).

* 2019-04-22, add book cover.

* 2019-04-08, improve formatting and link text in README ([`@katrinleinweber`](https://github.com/katrinleinweber), #137)

* 2019-03-25, add favicon ([`@wlandau`](https://github.com/wlandau), #136).

* 2019-03-21, improve Travis CI guidance, including link to examples. ([`@mpadge`](https://github.com/mpadge), #135)

* 2019-02-07, simplify code examples in Package Evolution section (maintenance_evolution.Rmd file) ([`@hadley`](https://github.com/hadley), #129).

* 2019-02-07, added a PDF file to export (request by [`@IndrajeetPatil`](https://github.com/IndrajeetPatil), #131).

## 0.1.5

* 2019-02-01, created a .zenodo.json to explicitly set editors as authors.

## First release 0.1.0

* 2019-01-23, add details about requirements for packages running on all major platforms and added new section to package categories.

* 2019-01-22, add details to the guide for authors about the development stage at which to submit a package.

* 2018-12-21, inclusion of an explicit policy for conflict of interest (for reviewers and editors).

* 2018-12-18, added more guidance for editor on how to look for reviewers.

* 2018-12-04, onboarding was renamed Software Peer Review.

## place-holder 0.0.1

* Added a `NEWS.md` file to track changes to the book.

# Review template {#reviewtemplate}

```

## Package Review

*Please check off boxes as applicable, and elaborate in comments below.  Your review is not limited to these topics, as described in the reviewer guide*

- [ ] As the reviewer I confirm that there are no [conflicts of interest](#coi) for me to review this work (If you are unsure whether you are in conflict, please speak to your editor _before_ starting your review).

#### Documentation

The package includes all the following forms of documentation:

- [ ] **A statement of need** clearly stating problems the software is designed to solve and its target audience in README
- [ ] **Installation instructions:** for the development version of package and any non-standard dependencies in README
- [ ] **Vignette(s)** demonstrating major functionality that runs successfully locally
- [ ] **Function Documentation:** for all exported functions in R help
- [ ] **Examples** for all exported functions in R Help that run successfully locally
- [ ] **Community guidelines** including contribution guidelines in the README or CONTRIBUTING, and DESCRIPTION with `URL`, `BugReports` and `Maintainer` (which may be autogenerated via `Authors@R`).

>##### For packages co-submitting to JOSS
>
>- [ ] The package has an **obvious research application** according to [JOSS's definition](http://joss.theoj.org/about#submission_requirements)
>
>The package contains a `paper.md` matching [JOSS's requirements](http://joss.theoj.org/about#paper_structure) with:
>
>- [ ] **A short summary** describing the high-level functionality of the software
>- [ ] **Authors:**  A list of authors with their affiliations
>- [ ] **A statement of need** clearly stating problems the software is designed to solve and its target audience.
>- [ ] **References:** with DOIs for all those that have one (e.g. papers, datasets, software).

#### Functionality

- [ ] **Installation:** Installation succeeds as documented.
- [ ] **Functionality:** Any functional claims of the software been confirmed.
- [ ] **Performance:** Any performance claims of the software been confirmed.
- [ ] **Automated tests:** Unit tests cover essential functions of the package
   and a reasonable range of inputs and conditions. All tests pass on the local machine.
- [ ] **Packaging guidelines**: The package conforms to the rOpenSci packaging guidelines

#### Final approval (post-review)

- [ ] **The author has responded to my review and made changes to my satisfaction. I recommend approving this package.**

Estimated hours spent reviewing:

- [ ] Should the author(s) deem it appropriate, I agree to be acknowledged as a package reviewer ("rev" role) in the package DESCRIPTION file.

---

### Review Comments
```





# Editor's template {#editortemplate}


```

### Editor checks:

- [ ] **Fit**: The package meets criteria for [fit](policies.md#fit) and [overlap](policies.md#fit)
- [ ] **Automated tests:** Package has a testing suite and is tested via Travis-CI or another CI service.
- [ ] **License:** The package has a CRAN or OSI accepted license
- [ ] **Repository:** The repository link resolves correctly
- [ ] **Archive** (JOSS only, may be post-review): The repository DOI resolves correctly
- [ ] **Version** (JOSS only, may be post-review): Does the release version given match the GitHub release (v1.0.0)?

---

#### Editor comments

---

Reviewers:
Due date:

```



# Review request template {#reviewrequesttemplate}

Editors may make use of the e-mail template below in recruiting reviewers.

```

Dear [REVIEWER]

Hi, this is [EDITOR]. [FRIENDLY BANTER]. I'm writing to ask if you would be willing to review a package for rOpenSci. As you probably know, rOpenSci conducts peer review of R packages contributed to our collection in a manner similar to journals.

The package, [PACKAGE] by [AUTHOR(S)], does [FUNCTION]. You can find it on GitHub here: [REPO LINK]. We conduct our open review process via GitHub as well, here: [ONBOARDING ISSUE]

If you accept, note that we ask reviewers to complete reviews in three weeks. (We’ve found it takes a similar amount of time to review a package as an academic paper.)

Our [reviewers guide] details what we look for in a package review, and includes links to example reviews. Our standards are detailed in our [packaging guide], and we provide reviewer [template] for you to use. Please make sure you do not have a [conflict of interest](https://devguide.ropensci.org/policies.html#coi) preventing you from reviewing this package. If you have questions or feedback, feel free to ask me or post to the [rOpenSci forum].

{IF APPLICABLE: The authors have also chosen to jointly submit their package to the Journal of Open Source Software, so this package includes a short `paper.md` manuscript describing the software that we ask you include in your review.}

Are you able to review? If you can not, suggestions for alternate reviewers are always helpful. If I don't hear from you within a week, I will assume you are unable to
review at this time.

Thank you for your time.

Sincerely,

[EDITOR]

[reviewers guide]: https://devguide.ropensci.org/reviewerguide.html
[packaging guide]: https://devguide.ropensci.org/building.html
[template]: https://devguide.ropensci.org/reviewtemplate.html
[rOpenSci forum]: https://discuss.ropensci.org/
```



# Approval comment template {#approvaltemplate}


```

Approved! Thanks <author(s) GitHub username(s)> for submitting and <reviewers' GithHub usernames> for your reviews! <optional: smiling cat emoji à la Scott>

To-dos:
- [ ] Transfer the repo to rOpenSci's "ropensci" GitHub organization under "Settings" in your repo.  I have invited you to a team that should allow you to do so.  You'll be made admin once you do.
- [ ] Add the rOpenSci footer to the bottom of your README
"```
[![ropensci_footer](https://ropensci.org/public_images/ropensci_footer.png)](https://ropensci.org)```"
- [ ] Fix all links to the GitHub repo to point to the repo under the ropensci organization.
- [ ] If you already had a `pkgdown` website, fix its URL to point to `https://docs.ropensci.org/package_name` and deactivate the automatic deployment you might have set up, since it will not be built centrally like for all rOpenSci packages, see http://devdevguide.netlify.com/#docsropensci. In addition, in your DESCRIPTION file, include the docs link in the `URL` field alongside the link to the GitHub repository, e.g.: `URL: https://docs.ropensci.org/foobar (website) https://github.com/ropensci/foobar`
- [ ] Add a mention of the review in `DESCRIPTION` via [`rodev::add_ro_desc()`](https://docs.ropensci.org/rodev/reference/add_ro_desc.html).
- [ ] Fix any links in badges for CI and coverage to point to the ropensci URL. We no longer transfer Appveyor projects to ropensci Appveyor account so after transfer of your repo to rOpenSci's "ropensci" GitHub organization the badge should be `[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/ropensci/pkgname?branch=master&svg=true)](https://ci.appveyor.com/project/individualaccount/pkgname)`.
- [ ] We're starting to roll out software metadata files to all ropensci packages via the Codemeta initiative, see https://github.com/ropensci/codemetar/#codemetar for how to include it in your package, after installing the package - should be easy as running codemetar::write_codemeta() in the root of your package.
<IF JOSS>
- [ ] Activate Zenodo watching the repo
- [ ] Tag and create a release so as to create a Zenodo version and DOI
- [ ] Submit to JOSS at <https://joss.theoj.org/papers/new>, using the rOpenSci GitHub repo URL. When a JOSS "PRE REVIEW" issue is generated for your paper, add the comment: `This package has been reviewed by rOpenSci: https://LINK.TO/THE/REVIEW/ISSUE, @ropensci/editors`
<IF JOSS/>

Should you want to acknowledge your reviewers in your package DESCRIPTION, you can do so by making them `"rev"`-type contributors in the `Authors@R` field (with their consent).  More info on this [here](https://devguide.ropensci.org/building.html#authorship).

Welcome aboard! We'd love to host a blog post about your package - either a [short introduction to it with one example](https://ropensci.org/tech-notes/) or [a longer post with some narrative about its development or something you learned, and an example of its use](https://ropensci.org/blog/). If you are interested, review [the instructions](https://github.com/ropensci/roweb2#contributing-a-blog-post), and tag @stefaniebutland in your reply. She will get in touch about timing and can answer any questions.

We've put together an online book with our best practice and tips, [this chapter](https://devguide.ropensci.org/collaboration.html) starts the 3d section that's about guidance for after onboarding. Please tell us what could be improved, the corresponding repo is [here](https://github.com/ropensci/dev_guide).
```




# NEWS template {#newstemplate}


```

foobar 0.2.0 (2016-04-01)
=========================

### NEW FEATURES

  * New function added `do_things()` to do things (#5)

### MINOR IMPROVEMENTS

  * Improved documentation for `things()` (#4)

### BUG FIXES

  * Fix parsing bug in `stuff()` (#3)

### DEPRECATED AND DEFUNCT

  * `hello_world()` now deprecated and will be removed in a
     future version, use `hello_mars()`

### DOCUMENTATION FIXES

  * Clarified the role of `hello_mars()` vs. `goodbye_mars()`


### (a special: any heading grouping a large number of changes under one thing)

    * blablabla.

foobar 0.1.0 (2016-01-01)
=========================

### NEW FEATURES

  * released to CRAN
```


# Book release guidance {#bookreleaseissue}


```

## Release book version <insert version>

### Repo maintenance between releases

- [ ] Look at the issue tracker for [the dev guide](https://github.com/ropensci/dev_guide/issues) and for [software review meta](https://github.com/ropensci/software-review-meta/issues) for changes still to be made in the dev guide. Assign dev guide issues to milestones corresponding to versions, either the next one or the one after that, e.g. [version 0.3.0](https://github.com/ropensci/dev_guide/milestone/2). Encourage PRs, have them reviewed.

### 1 month prior to release

- [ ] Remind editors to open issues/PRs for items they want to see in the next version.

- [ ] Ask editors for any feedback you need from them before release.

- [ ] For each contribution/change make sure the NEWS in Appendix.Rmd were updated.

- [ ] Plan a date for release in communication with `@stefaniebutland` who will give you a date for publishing a blog post / tech note.

- [ ] Draft a blog post / tech note about the release with enough advance for Stef to review it (1.5 weeks). [Example](https://github.com/ropensci/roweb2/pull/452), [General blog post instructions](https://github.com/ropensci/roweb2#contributing-a-blog-post). The editor writing the post is first author, other authors are listed by alphabetical order.

### Release


- [ ] Check URLs using [the corresponding script](https://github.com/ropensci/dev_guide/blob/master/inst/book_grooming.R).

- [ ] [Spell check](https://github.com/ropensci/dev_guide/blob/master/inst/spelling-check.R). Update the [WORDLIST](https://github.com/ropensci/dev_guide/blob/master/inst/WORDLIST) as necessary.

- [ ] Make a PR from the dev branch to the master branch, squash and merge it.

- [ ] Finish your blog post / tech note PR. Underline the most important aspects to be highlighted in tweets as part of the PR discussion.
```


