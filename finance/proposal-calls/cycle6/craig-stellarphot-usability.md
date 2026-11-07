### A suite of cloud-based photometry and astronomy education tools

**Proposal Category**: Innovations

### Project Team
Matt Craig will lead the project and do the bulk of the development work. Several
users will be solicited to provide feedback on usability of the tools and develop
a list of needs for their use cases.

### Project Description / Scope of Work
`stellarphot` is a package for aperture photometry of
stellar sources in a set of images. A related package,
[`astro-notebooks`](https://github.com/feder-observatory/astro-notebooks), provides a collection of tools for color image creation from monochorme images and for viewing and analyzing
light curves. Both have content that is broadly useful, and has been used primarily in a
cloud environment, but needs improvements to make it more broadly useful.



#### High Priority Objectives
+ "O6: Identify the barriers to making Astropy work easily in cloud contexts"
  while both packages above have been used in teach cloud-based astronomy courses,
  there are a number of rough edges in the user experience -- both for the novice users
  like students in a course and for the person setting up the cloud environment or
  who wishes to serve notebooks directly to novice users. This project will identify those rough edges and implement improvements to make the packages easier to use in cloud contexts.

#### Project / Work / Deliverables

1. **Usability testing program.** Recruit testers across several communities, provide them with a set of tasks to perform, and collect feedback on their experience. This will be done in two rounds, with the second round after the interface improvements are implemented.
   *Deliverable:* report on usability testing results and recommendations for improvements.
2. **Postage-stamp workflow.** Option in `ccdproc`/`stellarphot` to convert
   full-frame images into cutouts around the stars of interest, preserving them for
   future reanalysis without needing to keep the raw images.
3. **Robust differential photometry.** Implement a robust method for differential photometry that is less sensitive to outliers and can be used in the presence of clouds or other variable conditions.
   *Deliverable:* new functionality in `stellarphot` for robust differential photometry.
3. **Tutorials and workshop material.** Short task-focused notebooks usable
   in an undergraduate course and a half-day remote workshop
   targeted at educators and small observatories..
   *Deliverable:* notebooks in the package docs and workshop materials in a
   public repository.



### Approximate Budget
Currency: US $

- Project lead
- Honoraria for usability testers:
- TOTAL: ???

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
