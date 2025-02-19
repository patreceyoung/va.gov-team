# GMT yearly update
## What is this?
This document provides context and instructions on how to update the GMT year for the [Financial Status Report (Form 5655)](https://www.va.gov/manage-va-debt/request-debt-help-form-5655/introduction).  

## Background
The Financial Status Report (FSR) is for Veterans or service members who need help with debt related to VA benefit overpayments or health care copays. We have implemented a 'streamlined' version of the form, so veterans who meet specific criteria are not required to complete the entire form as a means to ease the stress and cognitive burden. 

These criteria for the streamlined version are set by our downstream partners (currently only at the VHA for health care copays). There are a number of factors considered for the streamlined version of the form, but they all depend on the Geographic Means Threshold (GMT). GMT is provided by a government service based on average income and number of dependents for a particular county. 

### How the sausage is made
The in depth process flow for GMT data moves from HUD -> VES -> CSV -> Income Limits database (based on an [initial convo](https://dsva.slack.com/archives/C52CL1PKQ/p1694702514600379) with the site wide public websites team). The Income Limits database is set up to serve the [Income Limits application](https://www.va.gov/health-care/income-limits/introduction), and the FSR leverages their database because it's the most digestible version of the data for our purposes. 

This flow is what makes things a little tricky for the update. The HUD updates based on previous fiscal year data, and that takes time to process and get approved, so the official numbers take a while to trickle down to the point where it's available to us. I'm not going to pretend to have a grasp on it, and I'm not sure it's completely relevant for this document, but context can be helpful. Point is, it'll be a good idea to conform with all parties we have access to, and are using the correct data. 

## What you actually came here for
### The business process
The two major players for us are our downstream partners at the VHA, and the team that manages the Income Limits database. 

1. Coordinate with downstream partners at VHA (usually via our PO) to confirm they are ready to start using the new year GMT data.
2. Contact the Income Limits team to confirm the database has been updated with the new year data.
3. Update FSR to use new year when pulling data from Income Limits endpoint when VHA is also ready to start using the new caluclations

### The `code` update
Updating the GMT year is pretty straightforward in the FSR, all of the relevant actions for fetching GMT data can be found in [geographicMeansThreshold.js](https://github.com/department-of-veterans-affairs/vets-website/blob/main/src/applications/financial-status-report/actions/geographicMeansThreshold.js). **The necessary update is just changing the `GMT_YEAR` constant to the new calendar year.** 
#### Note: 
Generally the year that is passed in is the calendar year (which pulls the previous fiscal year's calculations iirc). The income limits app does [a little -1 to the year in an internal process](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/income-limits-app/engineering/technical-architecture.md#geographic-means-test-gmt-threshold). It's best to spot check some different zip codes and number of dependents to confirm the data is there, and you can hit the URL directly (`/income_limits/v1/limitsByZipCode/${zipCode}/${GMT_YEAR}/${dependents}`) with some examples if you want to confirm with VHA the numbers match. 


## Resources
Here's a pile of links with hopefully relevant resources if you're into that kind of thing
### Code
 - [geographicMeansThreshold.js](https://github.com/department-of-veterans-affairs/vets-website/blob/main/src/applications/financial-status-report/actions/geographicMeansThreshold.js) (FSR file for fetching GMT data)
	 - [EmploymentQuestion.jsx](https://github.com/department-of-veterans-affairs/vets-website/blob/main/src/applications/financial-status-report/components/employment/EmploymentQuestion.jsx) (FSR page where we make the call)
### Links
- [HUD data source](https://www.huduser.gov/portal/datasets/il.html#data_2024)
- [Income Limits API Data Source and Migrations](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/income-limits-app/data/README.md#income-limits-api-data-source-and-migrations)
- [Income Limits Technical Architecture](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/income-limits-app/engineering/technical-architecture.md#geographic-means-test-gmt-threshold) 
### Some relevant tickets:
-  **[FSR] Update documentation for GMT year update [#90545](https://github.com/department-of-veterans-affairs/va.gov-team/issues/90545)** (Ticket for generating this documentation)
- **[FSR] Update GMT year for 2024 [#88120](https://github.com/department-of-veterans-affairs/va.gov-team/issues/88120)** (Title kinda says it all)
### DSVA Slack convos 
- [Initial implementation dialog with sitewide public websites team](https://dsva.slack.com/archives/C52CL1PKQ/p1694702514600379)
- [Another potentially helpful convo about some issues with zip codes that offers insight into year passed in vs data](https://dsva.slack.com/archives/C52CL1PKQ/p1698161355128349?thread_ts=1698156487.939009&cid=C52CL1PKQ )
- [2024 convo with sitewide team about updating year and formalizing process](https://dsva.slack.com/archives/C52CL1PKQ/p1722343494690099)

