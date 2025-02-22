# VA in-person appointment

## Overview

A scheduled in-person appointment at a VA facility.

## User stories

See [user stories for booked appointments](./all-appointment-types.md#booked-appointment-user-stories).

## Requirements

**Functional**
<!-- What the system should do in order to meet the user's needs (see user stories.) These are the aspects of the feature that the user can detect. -->

- Follows [requirements for canceling appointments](../tools/tool-cancel.md#requirements).
- Follows [requirements for adding appointments to calendar](../tools/tool-add-to-calendar.md#requirements).
- Follows [requirements for printing appointments](../tools/tool-print.md#requirements).
- User can review data and complete actions noted in the following table:

| Data and actions                                           | Confirmed | Upcoming | Past | Canceled |
| ---------------------------------------------------------- | --------- | -------- | ---- | -------- |
| Appointment Date and Time                                  | ✅         | ✅        | ✅    | ✅        |
| Status: Confirmed                                          | ✅         |          |      |          |
| Status: Past                                               |           |          | ✅    |          |
| Status: Canceled                                           |           |          |      | ✅        |
| Type of Care                                               | ✅         | ✅        | ✅    | ✅        |
| Provider Name                                              | 1          | 1         | 1      | 1         | 
| Facility Name                                              | ✅         | ✅        | ✅    | ✅        |
| Facility Address                                           | ✅         | ✅        | ✅    | ✅        |
| Directions Link                                            | ✅         | ✅        | ✅    | ✅        |
| Clinic Name                                                | ✅         | ✅        | ✅    | ✅        |
| Facility Phone Number                                      | ✅         | ✅        | ✅    | ✅        |
| Reason For Appointment                                     | ✅         | ✅        | ✅    | ✅        |
| [Add to Calendar Action](../tools/tool-add-to-calendar.md) | ✅         | ✅        |      |          |
| [Print Action](../tools/tool-print.md)                     | ✅         | ✅        | ✅    | 1        |
| [Cancel Action](../tools/tool-cancel.md)                   | ✅         | ✅        |      |


**Notes:**
1. Requirement not yet met 

## Specifications

**User flows**
- [Upcoming appointments](https://www.figma.com/file/xRs9s6QWoBPRhpdYCGc3cV/User-Flow?node-id=2019-19997&t=jIup4zOCLhBYNOvO-4)
- [Past appointments](https://www.figma.com/file/xRs9s6QWoBPRhpdYCGc3cV/User-Flow?node-id=127-22836&t=jIup4zOCLhBYNOvO-4)

**UI design specs**
- [Confirmed](https://www.figma.com/file/twogqAIoOL9WAFRqvUbwiS/VAOS-Templates?type=design&node-id=867-26448&mode=design&t=zfYBrRPZirDqa8uW-4)
- [Upcoming](https://www.figma.com/file/twogqAIoOL9WAFRqvUbwiS/VAOS-Templates?type=design&node-id=867-26544&mode=design&t=zfYBrRPZirDqa8uW-4)
- [Past](https://www.figma.com/file/twogqAIoOL9WAFRqvUbwiS/VAOS-Templates?type=design&node-id=867-26527&mode=design&t=zfYBrRPZirDqa8uW-4)
- [Canceled](https://www.figma.com/file/twogqAIoOL9WAFRqvUbwiS/VAOS-Templates?type=design&node-id=867-26536&mode=design&t=zfYBrRPZirDqa8uW-4)

**Page content**
- [Confirmed](../../content/appointment-details.md#va-in-person---confirmed)
- [Upcoming](../../content/appointment-details.md#va-in-person)
- [Past](../../content/appointment-details.md#va-in-person---past)
- [Canceled](../../content/appointment-details#va-in-person---canceled)

## Metrics
<!--Goals for this feature, and how we track them through analytics-->

- Goal 1
- Goal 2

**Events tracked**
<!-- Descriptions of events tracked on this page to meet those goals -->

- Event 1
- Event 2

[All events VAOS tracks](Link TBD)

## Alerts and conditional states
<!-- Any alerts that could display for this feature and what triggers them. -->

### [Alert description]
<!-- Add a new section for each alert -->

**Alert trigger**
[Description of what causes this alert to display]

**Alert UI**
- [User flow](Add link)
- [State template](Add link)
- [State content](Add link)

## Technical design
<!-- Endpoints and sample responses -->

**Staging URL:** [Add staging URL]

**Staging base URL:** https://staging-api.va.gov/

**Prod base URL:** https://api.va.gov/

**Endpoints**
`replace-with-endpoint-1`

`replace-with-endpoint-2`

To see the current api responses:
- Navigate to the [vets-api swagger](https://department-of-veterans-affairs.github.io/va-digital-services-platform-docs/api-reference/#/)
- Search for `https://api.va.gov/vaos/v2/apidocs`

<details>
  <summary>Sample response</summary>

```json
[Add sample response]
```

</details>

## Development testing
<!-- Unit tests, API tests -->

### [Call name] call

[How to use the VCR test framework](https://www.rubydoc.info/gems/vcr/VCR)
  
<details>
  <summary><b>VCR cassette</b></summary>

```
[Add VCR cassette]

```
</details>

<details>
  <summary><b>Example test for "[Call name]" that corresponds to the above VCR cassette.</b></summary>

```
[Add example test]
```
</details>
