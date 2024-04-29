Hi {RECIPIENT_NAME},
I'm writing on behalf of Astropy's Finance Committee regarding the outcome of your recent funding request [PR#{PR_NUMBER}](https://github.com/astropy/astropy-project/pull/{PR_NUMBER}). We have opened a new issue [#{ISSUE_NUMBER}](https://github.com/astropy/astropy-project/issue/{ISSUE_NUMBER}) to track the progress.

We are pleased to be able to let you know that, following consultation with the community, we are able to approve this request. **We can currently fund the Year 1 amount of ${DOLLAR} (US) to carry out the project**. Funding beyond this amount will be contingent upon the availability of funds. (We will be using the full budgets of all of the approved requests to craft future grant and funding proposals.) 

Ana Gabela and I will be your contacts on the Finance Committee to facilitate this award. Please get in touch with us if you have any questions or concerns. Please do not reach out to NumFOCUS directly.

In addition, new to this funding cycle, is the assignment of a COTR (Contracting Officer's Technical Representative) to each funded project. This concept is borrowed from government funding agencies, although it is to be stressed that Astropy's goal is to make the COTR role as low-overhead as possible. The COTR’s primary responsibility is to make sure the work is happening at the expected pace and, if necessary, to be a liaison between the funded project and the Finance Committee or CoCo. The COTR for your project will be assigned shortly and we’ll also be sending out more details about how we see this working.

If your request includes a new hire, please consult our newly compiled [hiring guide](https://docs.google.com/document/d/1xD8qdMW3GhPP86XR1fXE_9Cb03SxNtokgWG1Aoxor54/edit).

The next steps are:

{{ if INDEPENDENT_CONTRACTOR }}

* Please make sure that you are registered with Open Collective (https://opencollective.com): this is the system you will use to submit your invoices for payment. Note that your invoices should be submitted through the {PROJECT_NAME} ({PROJECT_URL}) project on Open Collective.
* We will reach out through NumFOCUS, Astropy's Fiscal Sponsor, to set up an “independent contractor agreement” (ICA; effectively a contract) and formal scope of work for the project.
* While this is in progress, the Finance Committee and the Coordination Committee will identify a COTR for each project. More information on this will be in the issue for your project once the COTR is identified.

{{ else if SUBAWARD }}

* You should reach out to your institution’s grant office to identify the relevant contact for your subaward. Make sure they know that NumFOCUS is the entity they will be working with for the subaward. 
* When your institutional contact has communicated to you the local process, reach out to me and we will identify the specific next steps required on your institution’s end. We will also start the process with NumFOCUS.
* While this is in progress, the Finance Committee and the Coordination Committee will identify a COTR for each project. More information on this will be in the issue for your project once the COTR is identified.

{{ end }}


We expect the work to be carried out between {START_DATE} and {END_DATE} (the “period of performance”). If you come to realize that the work will take more time than originally planned, you can apply for an extension following the procedure described at https://github.com/astropy/astropy-project/blob/main/finance/process/request-extension.md.

Congratulations --- we are really looking forward to seeing you put these funds to good use!

{FINANCE_POC_NAME} 
on behalf of the Astropy Finance Committee
