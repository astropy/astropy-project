### Cycle 6 Funding: Making Australian astronomical datasets accessible 

**Proposal Category**: Innovations

### Project Team
AAO Research Data & Software (RDS), Macquarie University  (aao.org.au) builds on
over 40 years of supporting Australian astronomy, from instrument control to
data reduction pipelines and data management tools. We run the Data Central 
science platform (datacentral.org.au) which relies on astropy and pyvo.

Proposed team (others may be involved as needed): James Tocknell, Anthony Heng,
Brent Miszalski, Simon O'Toole, and Nuria Lorente. Members have made individual 
contributions to astropy (including the current OAuth2 PR pyvo#785) but it is
our first proposal as a team, and we are keen to further contribute to this
important project not just through this proposal but in the longer term. 

### Project Description / Scope of Work
We propose two linked subprojects that open up data users struggle to reach.

1. Australian data in astroquery: astroquery is the touchstone for finding 
observational data, used by more than 4000 GitHub repositories (Astropy 
Collaboration et al. 2022, ApJ, 935, 167). Apart from astroquery.casda, 
Australian data are conspicuously absent. We will add access to the Anglo-
Australian Telescope (AAT) Archive and other Australian large survey datasets
hosted by Data Central: images, catalogues and spectra. These datasets 
complement upcoming Southern Hemisphere facilities such as the Vera Rubin 
Observatory (VRO), Cerenkov Telescope Array (CTA) and the Square Kilometre Array
(SKA). Many of these datasets are available via VO services, which many 
astronomers find hard to use. A dedicated astroquery module would lower that 
barrier. The AAT archive is not accessible via a VO service, and this work would 
allow programmatic access for the first time.

1. Modern authentication in pyvo: Most next-generation surveys, including LSST 
now under way, restrict data to survey partners, and many users hold rights to 
several surveys. pyvo.auth is built on the legacy IVOA SSO recommendation, which 
has had no reasonable implementation in five years and is now the bottleneck for 
restricted data. It is being replaced by the draft IVOA AuthVO recommendation, 
already being implemented on the data provider side by CADC, Data Central, ESA, 
Rubin and SKAO/SRCNet. As authors of PR pyvo#785 (a partial implementation), we 
plan to extend this work to bring pyvo into line with AuthVO, so that pyvo
users, and by extension astroquery users, can access Euclid, LSST, SKA and other
restricted datasets with their existing tools. Strong authentication is also one 
of the most effective defences against the AI bot traffic overwhelming online 
data services. As more services adopt it, pyvo must keep pace or astronomers 
will lose access.

#### High Priority Objectives
- **Identify single points of failure throughout the infrastructure of the 
Astropy ecosystem:** pyvo's reliance on the stalled IVOA SSO standard is a 
single point of failure for access to restricted VO data (part 2).
- **Identify the barriers to making Astropy work easily in cloud contexts:** 
authenticated access is a prerequisite for cloud-hosted archives and science 
platforms.

#### Project / Work / Deliverables
1. astroquery.datacentral (Budget options 1, 2, 3)
   - A new astroquery.datacentral module giving access to Data Central
   catalogues, images and spectra via its TAP, SIA and SSA services.
   - An API to the AAT Archive also hosted by Data Central, providing data 
   access from several instruments, the most prominent of which are 2dF and 6dF 
   MOS. We plan to provide new access to individual fibre tables for MOS data,
   providing unprecedented access to this rich spectroscopic database. 
   
1. pyvo authentication (Core, Budget options 1 & 2): Strategically refactor the
 current authentication system to align with the AuthVO approach, extending the 
 work started in pyvo#785. This PR only covers using the device code OAuth 2.x
 challenge. This will provide the first limited support of VO services
 supporting OAuth2.0 with pyvo.

1. pyvo authentication (Extension, Budget option 1): This will allow us to
   further improve support for a greater range of AuthVO-compliant VO services, 
   including:
   - Further OAuth 2.x flows (e.g. seamless authentication where a local 
   browser is available) and the other AuthVO authentication mechanisms, 
   including Basic/Digest and ivoa_cookie schemes, and additional authentication 
   modalities.
   - Add required integrations to other pyvo services such as TAPService, 
   SCSService, and DatalinkService to automatically discover and handle 
   authentication requests.
   - Automatic token refresh, so users need not re-authenticate on expiry.

### Approximate Budget
This funding application is to cover staff time at USD$188/hour. Recognising the 
size of the available budget, we propose three possible options for this work:

Option 1: astroquery + pyVO core + pyVO extension: Hours: 451; Budget: $84,500
Option 2: astroquery + pyVO core: Hours: 336; Budget: $63,000
Option 3: astroquery only: Hours: 210; Budget: $39,500

The minimum useful scope is Option 3. 
No travel funding is requested.

TOTAL: USD$84,500 (Option 1)

### Period of Performance
We expect the period of performance to be Jan 1, 2027 - Dec 31, 2027

