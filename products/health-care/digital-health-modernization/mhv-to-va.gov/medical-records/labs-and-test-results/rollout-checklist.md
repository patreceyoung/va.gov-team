# Lab and Test Results Phase 0 Readiness

### Phase 0 Overview 

Application exists on VA.gov in a published, authenticated state, but can only be found if users know the URL.  

### Phase 0 User Access:

- User links directly to new VA.gov tool via link provided in email. 

- MHV, My VA Health, or VA.gov will not link to the tool. 

- New tool will include “return to MHV” or “return to My VA Health” links.  

- Public websites, My VA continue to point users to the MHV application. 



## Phase 0: Pre-Rollout Readiness Checklist 

For an application to enter rollout Phase 0, the following must be true: 

 

### Go/No-Go Team 

- [X] Go-no-go team established 
     
- [ ] Review established definition of done for MVP 

- [ ] Go-no-go meeting(s) scheduled 
     - [ ] After readiness & staging review 
     - [ ] Accessibility is included  

- [ ] Team members and go/no-go decisions are added to the product decision log  

- [ ] Exit criteria for Phase 0 and entrance criteria for phase 1 agreed to by leadership 
 

### Communication  

- [ ] “Try this feature” email to “trusted users” is written, approved by leadership, and set up in Gov delivery 

- [ ] Email to trusted users is shared with contact center teams and coordinators  

- [ ] MHV SharePoint page announcing this shift is updated with information about phase 0 

 

### Change management  

-  Product guides developed and shared with: 

      - [ ] Contact Centers 

      - [ ] MHV Coordinators  

      - [ ] Facility POCs 

- [ ] Demo of new tool for audiences who will be affected by Phase 0 completed  

- [ ] Support staff trained

- [ ] Process for handling technical / customer support issues exists 

 
### Product 

- [ ] Intended product outcomes are documented and broadly communicated 

- [ ] Technical instrumentation is in place to track GA
      Required DD analytics in place, will convert to GA4 as its ready

- [ ] All steps of the collaboration cycle are complete
      Required Collab Cycle Phase 0 complete - as all domains are done we will go to final Collab Cycle 

- [ ] All the MUST feedback complete
      See above, all MUST feedback was completed for first domain, remaining domains go prior to Phase 1 launch

- [ ] Product documentation is reviewed by OCTO/OCC product managers & leads and determined to be complete and up-to-date 

- [ ] Establish email box for the feedback loop
      Email box set up for all Phase 0 domains and products
 
   
# Confirm with the following teams that they are ready for rollout: 

### User feedback / research  

- [ ] QA / user acceptance testing completed  

- [ ] Research documented in Github 



### Accessibility 

- [ ] Testing with complex cases (assistive tech users, cognitive disabilities, etc.) completed
      Ongoing accessibility testing is completed (domain by domain) - as mentioned above final staging review will happen as all domains are in Phase 0.
 

### UX/UI  

- [ ] Key design decisions added to decision log 

- [ ] Design documentation & briefs are up-to-date and linked in product Github 

- [ ] Breadcrumb suppressed during this phase, excluding the "Back" links when in sub-tasks

- [ ] Feedback link is in place in design and engaged, clicking it will open a link to send a feedback email. 

- [ ] Product content approved and QAd/copy edited

- [ ] FAQ content reviewed and approved by OCC, business owner, and where appropriate, subject matter experts.

 

### Engineering  

- [ ] Sign-in loads over the home page and pass next page parameter to send visitor directly to the tool after completing a successful sign on  

- [ ] All pages/components have latest content: _- All content is up-to-date with current designs. As new changes are made to the designs, development is implementing those as well_

- [ ] Unit test coverage is sufficient 

- [ ] Accessibility test coverage is sufficient _- All features requiring accessibility checks have been tested accordingly_

- [ ] End-to-end test coverage is sufficient _- e2e tests have been written for all functionality that requires it_

- [ ] Functional issues resolved 

- [ ] Engineering information documented and stored in GitHub 

- [ ] A temporary redirect is available at va.gov/my-health/ back to the tool until the My health landing page _- all links and redirects consistent with designs and other domains in Phase 0_
 

### Performance and Monitoring  

- [ ] Application performance SLOs exist 

- [ ] Downstream services tested at 2x average load for prior 12 months 

- [ ] DataDog monitors exist 

- [ ] Alerts exist 

   - PagerDuty - 

    - Slack - 

- [ ] On-call rotation exists - 

- [ ] Technical support escalation policy exists - 

 
### Analytics & Metrics  

- [X] Google Analytics 

    - Event tags exist 

    - Access 

    - Dashboard exists
     

- [ ] Domo 
    - Access

    - Dashboard exists 
- [X] Datadog 
     - Access 

     - Dashboard exists 

     - RUM code implemented


### Legal & Policy  

- [ ] Application reviewed for potential legal implications 

- [ ] Application reviewed for adherence to policies 

- [ ] Application reviewed for information accuracy and patient safety 
