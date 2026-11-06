### Consolidate and improve dashboard efforts to monitor coordinated and affiliated package health

**Proposal Category**: Innovations

### Project Team

This proposal is to fund the following people at [Aperio Software](https://aperiosoftware.com):

* Thomas Robitaille
* Stuart Mumford

This could also fund other individuals working at Aperio Software if required.

### Project Description / Scope of Work

Over the last few years, several attempts have been made to develop dashboards to monitor the status of coordinated and affiliated packages.
In this project we plan to consolidate these efforts to provide a 'live' dashboard with up-to-date information on the maintenance status, as well as continuous integration and interoperability status of coordinated and affiliated packages.
We will then use this to identify packages in need of maintenance,

#### High Priority Objectives

This work will directly address objective [O5](https://astropy-roadmap.readthedocs.io/en/latest/#o5-improve-the-sustainability-and-maintenance-of-coordinated-and-affiliated-packages) of the Astropy roadmap (Improve the sustainability and maintenance of coordinated and affiliated packages) and specifically will complete the following key results:

* **KR5.1** A dashboard exists to show automated health metrics for coordinated and affiliated packages
* **KR5.2** Criteria are published for automatically determining when a package needs help with maintenance
* **KR5.3** An issue is opened on the astropy-project repo for every package failing the criteria, in order to discuss a plan to help improve maintenance and sustainability

While these issues will then be used towards KR5.4 (agreeing a plan forward for three of the packages), we cannot commit to completing this key result since this whether an agreement is reached or not will be outside of our control and this may involved e.g. the coordination or strategic committees.

#### Project / Work / Deliverables

The following dashboards currently exist for Astropy:

* https://dashboard.astropy.org - this is the oldest effort. This shows for all coordinated, infrastructure and affiliated packages status badges from e.g. CI, coverage, ReadTheDocs, PyPI, and so on. However, the infrastructure for this was last updated 7 years ago (it still shows Travis CI status for example), and while build statuses and coverage are useful live metrics, information such as the last version on PyPI is not useful without knowing how old it is (and likewise there is no indication of the age of the status badges)

* https://www.astropy.org/astropy-integration-testing/ - this is a recent effort to do integration testing on all coordinated and affiliated packages, checking whether the test suites of all the packages pass when they are installed in an environment with all other packages.

SunPy developers have also built a dashboard at https://sunpy-dashboard.cadair.dev/dashboard/ which is more useful for checking the detailed CI status of packages, getting live views into passing/failing jobs on ``main``.

In this work, we propose to work on and extend these different efforts in order to build a single platform which may include one or multiple dashboards that can be used to monitor the health of the coordinated and affiliated ecosystem.
In addition to being able to monitor information already shown by the efforts above, we propose to also extend this to include metrics such as time since last release, time since last commit, statistics about maintainers and pull requests in the last year.
The goal would be to replace https://dashboard.astropy.org with the new content to provide a single point of access to this information

Based on this, we will then develop criteria to help us flag packages in need of attention/maintenance.

### Approximate Budget

80h @ USD 150/hour = USD 12,000

### Period of Performance

Jan 1, 2027 – Dec 31, 2027
