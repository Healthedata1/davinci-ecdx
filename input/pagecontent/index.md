
<div class="bg-info" markdown="1">
Publishing Punch list:

- [ ] Finish [Resolving Trackers](https://jira.hl7.org/secure/Dashboard.jspa?selectPageId=11801)
- [ ] Finish Applying Resolved Trackers
- [ ] QA
- [ ] Reconciliation Spreadsheet
- [ ] publication checklist

Where possible, new and updated content will be highlighted with green text and background
{:.new-content}

{{ site.data.pl.list[0].desc }}

</div>

This IG provides detailed guidance that helps implementers use FHIR-based interactions to support specific exchanges of clinical data between providers and payers (or other providers).  What is unique about this guide is that it documents the **Direct Query**, **Task Based** and <span markdown="1" class="bg-success">**Attachments** transaction approaches for requesting and sending information</span>. Key scenarios this IG can support include:

 - Requesting *attachments* to support claim submission, medical necessity and other reasons for attachments between payers and providers
 - Gathering information for Quality programs and Risk Adjustment between payers and providers
 - Exchanging clinical data between referring providers
 - {:.new-content}Sending unsolicited and solicited attachments for claims

<span markdown="1" class="bg-success">In the context of this guide, 'clinical data' means *any* information a provider holds in a patient's health record.</span> The data format is not limited to FHIR resources, but includes C-CDA documents, pdfs, text files and other types of data. There may be requests for payloads of clinical records of care such as CCD Documents, clinical data sets that may be represented in a FHIRBundle (or [C-CDA on FHIR Documents](http://hl7.org/fhir/us/ccda/)), and clinical data such as a specific FHIR resource.

By using the FHIR standard and implementing this guide, payers can be explicit about the data they are requesting as opposed to general requests which often result in providers sending more information than is necessary. The anticipated benefit of using FHIR is more efficient and effective exchange of health record information in several areas such as claims management, care coordination, risk adjustment and quality reporting.

This IG provides several *general* examples to illustrate the different approaches for exchanging clinical data, but it does not to document specific use cases.  We plan to create a set of [Clinical Data Exchange- Supplemental Guides] which will document and provide examples for specific use cases.
{:.bg-info}

### About This Guide

This Implementation Guide is supported by the [Da Vinci] initiative which is a private effort to accelerate the adoption of Health Level Seven International Fast Healthcare Interoperability Resources (HL7® FHIR®) as the standard to support and integrate value-based care (VBC) data exchange across communities. Like all Da Vinci Implementation Guides, it follows the [HL7 Da Vinci Guiding Principles] for exchange of patient health information.  The guide is based upon the prior work from the [US Core] and [Da Vinci Health Record Exchange (HRex)] Implementation Guides. Changes to this specification are managed by the sponsoring HL7 [Patient Care (PC)] workgroup and are incorporated as part of the standard HL7 balloting process. You can suggest changes to this specification by creating a *change request tracker* by clicking on the [Propose a Change] link at the bottom of any page.

#### How to read this Guide

This Guide is divided into several pages which are listed at the top of each page in the menu bar.

- [Home]\: The home page provides the introduction for the Da Vinci Clinical Data Exchange Project.
- [Background]\: This page provides the background and a summary of the Da Vinci Clinical Data Exchange Project.
- Specification\: The Specification pages provides specific guidance on exchanging clinical data between Payers and Providers:
  - {:.bg-success}[Exchanging Clinical Data]\: Exchanging Clinical data overview page.
  - {:.bg-success}[Direct Query]\: Payer directly queries EHR for specific data using the standard FHIR RESTful search
  - {:.bg-success}[Task Based Approach]\: Payer identifies the ‘type’ of information desired and the EHR supplies the data possibly with human involvement to find/aggregate/filter/approve it.
  - {:.bg-success}[Attachments]\: Documents how to exchange attachments for claims or prior authorization using a FHIR based `$attachments` operation. *This content is to be considered DRAFT, because it has not yet undergone HL7 balloting.*
- {:.bg-success}[Signatures]\: This page provides specific guidance and rules to exchange *signed* data using FHIR and non FHIR signatures.
- {:.bg-success}[Security and Privacy]\: This page provides general expectations to ensure security, privacy, and safety of Da Vinci CDex exchanges.
- {:.bg-success}[FHIR Artifacts]\: These pages provide detailed descriptions and examples for Task based data exchange approach.
- [Downloads]\: This page provides links to downloadable artifacts.

---

**This Implementation Guide was made possible by the thoughtful contributions of the following people and organizations:**

- *The twenty-two founding [Da Vinci Project](http://www.hl7.org/about/davinci/index.cfm?ref=common) member organizations.*

- *Eric Haas, Health eData Inc*
- *Lloyd Mckenzie, Gevity*
- *Robert Dieterle, EnableCare*
- *Viet Nguyen, Stratametrics*
- *Jocelyn Keegan, Point of Care Partners*
- *Lisa Nelson MaxMD*
- *Rick Geimer Lantana Consulting Group*

---

<br />

{% include link-list.md %}
