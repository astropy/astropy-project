### Title
Cycle 4 Funding: Making Australian astronomical datasets accessible 

### Project Team
AAO Research Data & Software, Macquarie University  (rds.org.au) 

The foundation of the AAO Research Data & Software (RDS) team is built upon over 
40 years of supporting astronomical observatories in Australia. This software 
development experience ranges from controlling telescopes and their instruments, 
to building data reduction pipelines, to developing and implementing tools that 
store, manage, and analyse data. The RDS team aims to be at the forefront of 
research software and data engineering. We look for the best technology to solve
a problem, but at the same time realise that software is not innovative or useful
if it cannot be maintained, extended, or scaled. We appreciate the benefits that
a holistic view of a software ecosystem can bring, but also recognise that a 
"deep dive" might be necessary to solve a complex problem. And while our historical
strength has an astronomical flavour, our skills and expertise are increasingly 
recognised across research disciplines. Some of our current and recent projects 
include the Data Central Science Platform, including Virtual Observatory services; 
VLT MAVIS Data Reduction pipeline design and development; our state-of-the-art 
Pipelines as a Web Service (PAWS) system; and our recently completed ESO VLT 
Pipelines development and maintenance project.

We propose the following individuals for this project, although other team members 
can be involved if needed:

* James Tocknell
* Anthony Horton
* Brent Miszalski
* Nuria Lorente
* Simon O'Toole

Although this is our first proposed contribution to astropy as a team, some of
our members have made individual contributions over the years. Moreover, given
the use that we make of astroquery in our Data Central science platform
components in particular, we are keen to further contribute to astroquery
infrastructure, not just through this proposal, but also in the longer term.

### Project Description
The astroquery package has become a popular touchstone for observational 
astronomers to find data, being used by more than 4000 github repositories (The 
Astropy Collaboration et al. 2022, 935, 167). Apart from astroquery.casda, 
Australian astronomical data are conspicuously absent from astroquery. In this 
project we address this shortcoming by adding access to the Anglo-Australian 
Telescope (AAT) Archive and several other Australian large survey datasets hosted
by Data Central (https://datacentral.org.au): images, catalogues and spectra. 
Enhancing the visibility and accessibility of Australian datasets is critically 
important to complement multi-wavelength and multi-messenger observations from 
upcoming Southern Hemisphere facilities such as the Vera Rubin Observatory (VRO), 
Cerenkov Telescope Array (CTA) and the Square Kilometre Array (SKA). 

While many of the datasets we plan to add are accessible via VO services, many 
astronomers find VO services very difficult to interact with. Adding them to their 
own dedicated astroquery module would alleviate their anxieties about using these
services. The AAT archive, on the other hand, is not currently accessible via a 
VO service and this work would allow for robust programmatic access for the 
first time. 

We also propose to address a longstanding problem in the preparation of multi-object 
spectroscopy (MOS) observations by adding the Cone of Darkness algorithm 
(Lorente 2014, ASPC 485, 95) to select blank sky positions. This automates a 
tedious task in a robust manner for any input astroquery catalogue. 


### Project / Work
1. Data Central catalogues, images and spectra are accessible, respectively, via 
TAP, SIA and SSA services hosted by Data Central. We plan to provide access via 
a dedicated astroquery.datacentral module. The module would also include an API 
to access the AAT archive, also hosted by Data Central. The AAT archive hosts data 
from several instruments, the most prominent of which are MOS observations taken 
with the 2dF and 6dF facilities, amassing vast quantities of spectroscopic data. 
Via improvements to the archive API endpoints, we plan to provide access to the 
individual fibre tables of MOS observations, providing unprecedented access to 
this rich spectroscopic database. In the case of 2dF-AAOMega observations, users 
may then request automatic reductions of queried spectra via our Pipeline As a 
Web Service (PAWS) system.

1. Addition of the Cone of Darkness algorithm involves porting the C++ code and 
tests to astroquery such that any input catalogue (also obtained with astroquery) 
may be used to select sky positions. High proper motion stars may be excluded 
with an optional GAIA DR3 query.


### Approximate Budget
This funding application is to cover staff time. We estimate 420 hours of effort
are required to complete this project, which at an hourly rate of USD$145/hour 
gives a budget of USD$60,900.

This effort estimate will be refined, and the minimum useful time to carry out
some of the proposed work will be determined and added here during the iteration
period.


### Period of Performance
We expect the period of performance to be two years.
