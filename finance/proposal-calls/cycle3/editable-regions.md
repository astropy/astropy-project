### Title
Complete effort on gui-editable regions

### Project Team
Adam Ginsburg
Derek Homeier
Aperio Software

### Project Description
The ["Linking CASA to the astropy ecosystem"](https://science.nrao.edu/facilities/alma/science_sustainability/Spectral_Cube_and_Radio_Beam_Ginsburg.pdf)
[Cycle 7 ALMA Development project](https://science.nrao.edu/facilities/alma/science_sustainability/alma-develop-history) funded development to make regions editable in 
matplotlib interactive GUI windows.  However, we ran out of funding before the work could be completed.  There are several open PRs in regions:

 * [Support for rotation](https://github.com/astropy/regions/pull/390)
 * [Support for polygons](https://github.com/astropy/regions/pull/406)

and in matplotlib:

 * [Rectangle rotation](https://github.com/matplotlib/matplotlib/pull/21945)
 * [weird aspect ratios](https://github.com/matplotlib/matplotlib/pull/21886)
 * [polygon rotation](https://github.com/matplotlib/matplotlib/pull/22159)

that need to be wrapped up.  Then, significant documentation is needed to show users how to use these cool tools.

### Project / Work
The main work is to complete the above PRs and write new documentation

### Approximate Budget
Currency: US $20,000 estimated.

All will be used to cover effort by Aperio Software team members.

The minimum allocation to make this effort viable is $5,000, which accounts for ~10h of ramp-up time for an individual to dig into and understand the present state of PRs, plus ~40h of effort to make appropriate changes, assuming an hourly rate of $100/h
