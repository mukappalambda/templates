# [Project Name] Eng Design Doc

[toc]

---

## Team

You (Project Tech Lead, Engineer)
Your Collaborators (Engineer)

---

## Objective 

> Briefly describe the purpose of this service or application. Link to the project plan if applicable. Consider answering:
- Why are you building this component? 
- What is the long term purpose?

### Goals

> List the concrete goals you plan to achieve with this component. This should be an expansion of the objective. Consider:
- Customer requirements
- User outcomes
- Deprecations - what could we remove from our existing infrastructure when this exists?

### Non-goals

> List specific things you are NOT trying to achieve. Consider:
- Areas of potential scope creep
- Areas of potential confusion

---

## Architecture / System Design

> If needed, give a high level summary of your design. Delete any section below that is irrelevant to your project, and add any with Heading 4 based on the prompts

### Diagram

> A picture is worth a thousand words. Summarize your design with a diagram here

### Previous Design

> Summarize or diagram the existing design, in particular contrasting how the current design differs and solves existing problems

### Datastore

> Specify the following aspects of the datastore, as needed:
- Schema
- Type and rationale (MySQL, Oyster, ElasticSearch, etc)
- Input/output
  - How is the service consuming the data?
  - What are the data contracts?
  - What does your service depend on?
  - What is going to depend on your service?
  - Any dependencies on shared datastores (e.g. airmaster, calendar db)?
  - Are you introducing any new infrastructure components (e.g. key value store)? Which ones?
- Data migration and bootstrapping

### APIs

> Specify the public API that your component has. Consider:
- REST service APIs
- Client libraries

### [Detailed Design Sections]

> If needed, explain the details of other aspects of your design. May include: 
- Data quality
- Structured data logging
- Rollout and/or migration plans
- Constraints and performance considerations
  - What read/write volume does it need to handle?
  - What other constraints does this face: does it need to be embeddable in another service, or run on other boxes? Are there memory constraints?

### Stakeholders

| Person | Role | Details and/or Comments |
| ------ | ---- | ----------------------- |
|        |      |                         |
		
---

## Alternatives Considered

> This should be one of the most important parts of your design doc: it helps people understand why you chose the above, and what things you’ve already thought about and ruled out. You should include:
- What options did you consider?
- Why are each of those options unworkable?

---

## Operations

### Monitoring and Metrics

Consider:
- What kind of metrics/counters can be added? success/error/decline rate, stuck txns count, backlog count, etc.
  - How can those counters/metrics be used to detect potential issues?
- What kind of monitoring/alerts will be set up? For example:
  - Count of success, failure, rejection
  - Success or failure rate

### Failure Modes

> Consider the following questions and describe failure handling as needed:
- What happens when one of your dependencies goes down?
- What happens when your system/service goes down?
- How easy is it to bring them back up?
- Is there data loss?
- How complex is the deployment process
- How do you rollback?
- How much maintenance do you need after launch?
> You don’t need to answer all of these if it’s obvious — i.e. you’re using well-understood components — but should answer some of these as they apply to your project

### Scaling

> How will your component scale long term?
- What if usage grows by 5x? 20x?
- Do you have a story for someday handling 20x?
- Does it scale well horizontally?
- What is your load testing plan?

---

## Timeline

- What is your launch timeline?
- What is your migration plan, if applicable?
- What are you not doing now?
- What could/should be done to improve this later on?
 
> List out your dependencies here, in particular ones that are on your critical path and may not be complete or present a non-trivial risk

---

## Technical Debt

> Is any technical debt being introduced by this work? What is the specific plan for addressing this?

---

## Risks

> Identify risks that may impact the project’s success. Some things to think about include: key stakeholders outside the project not being available for reviews, additional stakeholders needed. A few minutes of thinking here will help ensure mitigations are created for issues that may occur during the project.
- Risk ~= likelihood & impact
- Think along both these dimensions
- Enter risks in the table below from most impactful upon the project at the top, to least impactful at the bottom

| Description | Likelihood & Impact (Low/Med/High) | Mitigation Summary | Links / Comments |
| ----------- | ---------------------------------- | ------------------ | ---------------- |
|             |                                    |                    |                  |

---

## Feedback

> Include a summary of the major feedback and reviews here. Detailed feedback should be tracked in comments, high level outcomes in this table.

| Date | Name | Notes |
| ---- | ---- | ----- |
|      |      |       |

---

## Links

> Include links to supporting docs here
