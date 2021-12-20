# Notes

## Impact Metrics
In practice, Impact metrics are often owned by Product Managers, and companies that do goal-setting with something like Objectives and Key Results (OKRs) use Impact metrics to align teams.

In a modern product development organization, agreeing on the objectives and outcomes is a way to empower the teams, as Marty Cagan and Chris Jones write in the 2020 book Empowered.

Another way to think about Impact is through the investment you're making. Do you understand how much of your engineering effort is going to your company's top priorities, used for keeping the lights on, dealing with technical debt, etc?

The reality is that sometimes it's difficult to attribute changes in business metrics to individual actions. It is more effective to understand how much you're investing in specific priorities and see if that investment is getting you what you want.

## Flow 

**Are we delivering continuously without getting stuck?**

Understanding the flow of work is critical because many of the issues are systemic. Even the most talented developer might not have the full picture of how much time is being wasted when work is bounced between the teams, half-completed features are put on the shelf as priorities change, or all the code gets reviewed by just one person. It's easy to think that you're solving a quality problem by introducing code freezes and release approvals, but in reality, it might not be worth it.

Flow of work is often measured in terms of cycle time. The term cycle time comes from manufacturing processes, where cycle time is the time it takes to produce a unit of your product, and lead time is the time it takes to fulfill an order (from a request to delivery).

When talking about cycle time for code, we're talking about the time it takes for code to reach production through code reviews and other process steps. Sometimes it's called change lead time.

Cycle time is the most important flow metric because it indicates how well your “engine” is running. The point is not to worry about slow activity but rather the periods of inactivity.

## Deployment Frequency

Deployment frequency & error rate
Depending on the type of software you're building, "deployment" or "release" might mean different things. For a mobile app with an extensive QA process, getting to a two-week release cadence is already a good target, while the best teams building web backends deploy to production after each change.

Deployment frequency doubles both as a throughput metric and as a quality metric. When a team is afraid to deploy, they'll end up doing it less frequently. Solving the problem typically requires building more infrastructure. Some of the main considerations are:

## Wrong metrics

nother traditional management pitfall is to focus on utilization, thinking that you want your developers to be 100% occupied. While it's true that 0% utilization is likely a signal about some problems, maximizing it will only lead to worse problems. As the utilization approaches 100%, the cycle times shoot up.

There's a time and place for metrics around individual developers. In very healthy environments they could be used to improve the quality of coaching conversations while understanding the shortcomings of these measures. Unfortunately, in a bigger organization, an effort to focus on individual metrics is likely to derail your good intentions around data-driven continuous improvement.

## Health

The last dimension to measure is the health of the team. Good development practices are the foundation for a sustainable pace of working. It's also what keeps the team performing in the long run.

I used to ask my teams at Smartly.io to react to these statements every six months:

- The team's bug backlog is manageable

- The team has all the skills needed to build the products in their area

- The team is able to test new product ideas with customers

- The team constantly delivers work in small increments

- The team doesn't have significant technical silos or abandoned features

- The team's work is not blocked by other teams

- The team has communicated a clear vision and how to get there

- We feel safe to challenge each other, and our work is transparent

## Measuring Collaboration

It's not obvious what a good level of collaboration is and how to measure it.

We can measure:

- **Features:** Having multiple developers working on the same feature means that people need to understand the same corner cases about the business domain. Even if it's a mobile developer and a backend developer working together, they share the definitions of the complex domain concepts.

- **Codebases:** If a codebase has only been touched by one person, it's going to get increasingly difficult to onboard someone else to it. In a bigger codebase, this can be even applied at the file level.

## Testing:

There are measures like code coverage that can be used for tests, but their applicability depends on your choice of technologies. For example, in a statically typed language, you might want to test different things than with a dynamically typed language.

The important thing is that the team agrees on how to test and does it consistently. Bug fixes should have a test. Features should have a test coverage that makes sense in your context. In fact, research shows that a high number of tests is a better indication of quality than code coverage.

It's also useful to understand if test flakiness is causing problems, and when your test suite is starting to take a long time (15+ minutes) to run.

## DORA
The 4 DORA (Accelerate) Metrics
The DORA group found that elite performing software teams – those who deliver the most value, fastest, and most consistently – will optimize for four metrics in particular:

**Change Lead Time**

Change lead time measures the total time between when work on a change request is initiated to when that change has been deployed to production and thus delivered to the customer. Lead time helps you understand how efficient our development process is. Long lead times may be the result of some inefficient process or bottleneck along the development or deployment pipeline. 

The most common way of measuring lead time is by comparing the time of the first commit of code for a given issue to the time of deployment. A more comprehensive (though also more difficult to pinpoint) method would be to compare the time that an issue is selected for development to the time of deployment.

**Deployment Frequency**

Deployment Frequency measures how often a team pushes changes to production. This indicates how quickly your team is delivering software – your speed. DORA tells us that high performing teams endeavor to ship smaller and more frequent deployments. This has the effect of both improving time to value for customers and decreasing risk (smaller changes mean easier fixes when changes cause production failures) for the development team.

**Change Failure Rate**

Change Failure Rate is a measurement of the rate at which production changes result in incidents, rollbacks, or failures. This tells you the quality of code you are pushing to production. The lower the rate here the better (higher performing teams have a change failure rate of 0-15%), but the ultimate goal of the team here should be to decrease the change failure rate over time as skills and processes improve. 

The trickiest piece for most teams is in defining what a failure is for the organization. Too broad or too limiting of a definition and you will encourage the wrong behaviors. In the end, the definition of failure is and needs to be unique to each organization, service, or even team.

**Mean Time to Recovery (MTTR)**

MTTR is about resolving incidents and failures in production when they do happen. It is the measurement of the time from an incident having been triggered to the time when it has been resolved via a production change. The goal of optimizing MTTR of course is to minimize downtime and, over time, build out the systems to detect, diagnose, and correct problems when they inevitably occur.

## Bibliography

- https://www.geeksforgeeks.org/software-measurement-and-metrics/
- https://www.swarmia.com/blog/measuring-software-development-productivity/
- https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance
- https://jellyfish.co/blog/dora-metrics-101/