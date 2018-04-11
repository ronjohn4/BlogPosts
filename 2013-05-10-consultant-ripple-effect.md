# Consultant Ripple Effect<br>2013-05-10<br>teams<br>
---
  
Several years ago the executive team at my company has decided to use a consulting firm to implement several features our internal staff hasn't had time to get to.  Our pride initially takes a hit but after reason sets in, we realize that these are features we want, if we can get some additional horsepower then great.  The first phase of the engagement is coming to and end and the design is now seeing the light of day.  Along with the design are assumptions and choices that have been made with input from the executive team but without the input of support staff members.  These ripples will flow through all departments in the company following implementation and continue to reverberate through the halls of our normal workday for years.  


Don't get me wrong, I enjoy working with consultants.  They bring fresh ideas, new perspectives and a sense of urgency that is sometimes lacking in the day to day workings of the employee proletariat.  The Project Manager in me uses consultants to level out an uneven workload.  The Engineer in me uses consultants for knowledge transfer or simply to accomplish a task involving technologies that my staff shouldn’t spend time becoming proficient with.

Sizzle vs. maintenance was the first issue that jumps out of the proposal.  There are several requirements that have been sticking points all of which directly tie back to the platform; web based.  The aggressive timeline we’ve maintained for the last 4 years makes UI features like drag and drop a luxury we had to live without.  The scope of the consulting proposal covers all of these features.   Great!  Where do we sign?  Wait a minute, the timeline is shorter than I would expect.  A little digging discovers that they plan to use Microsoft Silverlight.

The plumbing shouldn’t be a surprise.   Several of the requirements are a heavy tax on our MS SQL Server from a query perspective.  No dig intended, the queries are simply monsters.  The consulting proposal is to use OLAP which is architecturally correct.

Both the OLAP and Silverlight aspects of the proposal create a maintenance challenge.  We are expected to not only to live with the deliverables but to maintain them going forward.  OLAP is one of those technologies you can’t pretend to know.  We either need to ramp up on training or hire a full time DBA; given our current crunch we should hire.  Silverlight on the other hand can be covered by our current development staff with a little training.

QC currently utilizes an automated testing tool that I have little hope will support Silverlight.  This means either testing by hand or the expense of purchasing and learning a new automated testing tool.  Additionally the fine print in the consulting proposal reveals that our internal QC staff is expected to test the new solution. 

Project Management needs just ratcheted up on the complexity scale.  The pessimist in me views the QC work as an escape hatch for the consultants if the project goes south.  It falls on us to apply PM to a high degree to keep expectations clear. 

Future development (internal or consulting) has a new expectation from management and our user base to contend with.  Silverlight allows for some powerful UI functionality that will now be expected from all future work.  We’ve set a high velocity expectation by becoming extremely proficient at rolling out features with straight ASP.NET, this velocity will be expected even if we need to use Silverlight going forward.

So there you have the possible downside of this engagement for the internal IT staff;  OLAP, Silverlight, new QC tools, additional PM responsibilities and the expectation that our future work will be performed at the level.

But wait a minute.  This consulting engagement definitely has a glass half full aspect.  Managed correctly our internal staff can acquire new skill sets through training, experience with newer technologies and gain a reputation for delivering a better user experience.  The Consulting Ripple Effect may be a positive influence for the company and the individuals making up the IT staff for years to come if managed closely and approached offensively rather than defensively.

  

