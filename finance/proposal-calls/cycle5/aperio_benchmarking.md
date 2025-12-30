### Reliable performance benchmarking for the Astropy project

### Project team

This proposal is to fund the following people at [Aperio Software](https://aperiosoftware.com):
* Thomas Robitaille
* Stuart Mumford
This could also fund other individuals working at Aperio Software if required.

### Project Description / Scope of Work

The goal of this project is to set up a dedicated physical server in a way that can be used to run the astropy benchmarks.

#### Roadmap Items

This project will address the following roadmap item:

- :large_orange_diamond: Maintain and improve robust performance benchmark reporting.

#### Project / Work / Deliverables

The main tasks in this project are:

* Rent a commercially available dedicated physical server
* Set up the server as a GitHub self-hosted runner (taking care to bind the runner to a specific core if possible to ensure stable timings)
* Update the existing astropy core package continuous integration to use this runner for the pull request benchmark run, and tighten the threshold for performance regressions (since it should be possible to with more accurate timings)
* If time allows, add a new CI job which runs on ``main`` which will run the latest benchmarks and push the latest asv dashboard to GitHub pages to monitor

The aim here is to keep the server configuration minimal and keep all the details about how to do the benchmarking in the CI configuration, to facilitate any potential future server migration, and ensure that project members can collaboratively work on improving how the benchmarking is done.

### Approximate Budget

The breakdown of the budget is as follows:

* USD 50/month for server rental
* 40 hours @ USD 150/hour for server set-up and development work

The total requested amount is USD 6600

### Period of Performance

Jan 1, 2026 to Dec 31, 2026
