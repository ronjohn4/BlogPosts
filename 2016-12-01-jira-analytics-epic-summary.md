# JIRA Analytics - Epic Summary<br>2016-12-01<br>agile<br>
---
I recently worked with a team that had a very 'mixed' backlog. After some heavy clean up, the backlog was well grouped by Epic. This allowed us to discuss and make decisions at the Epic level. What we needed now was a more detailed view into the statistics at the Epic level. We needed to show: 

  1. The status of the Epics
  2. Which Epics have work started
  3. Which Epics are read to work
  4. Roughly the size of each Epic
  5. Epics that need attention - work items are flagged

I ended up writing a simple Python command line tool that outputs a CSV file. CSV is easy to open with Excel and makes the interpretation done by a human easier. [![jra-stats](http://ronjohnsonconsulting.com/wp-content/uploads/2016/12/JRA-Stats-1024x325.png)](http://ronjohnsonconsulting.com/wp-content/uploads/2016/12/JRA-Stats.png) **Table 1 - CSV statistics opened in MS Excel** The first thing we noticed was not statistics based. The Epic names pointed out that the work was grouped by Phase. An Epic with the name 'Logging Improvements' has much more meaning than Product X - Phase 2'. It was apparent that we needed to start grouping our work to describe 'What' was being done. 

## The Stats

On the included sample output (Table 1 above), I've numbered in red some observations that were interesting. 

  1. It appears that there is some churn in ranking at the Epic level. Several Epics at lower ranking are In Progress while higher ranked Epics are still in Design or Ready.
  2. UTIL-754 is all bugs. Is this because it is new or is it really an Epic to squash bugs?
  3. Here we see that 8 Stories are sized but there are 9 in this Epic. This means there is still a Story to size and the Epic is In Progress, time to size that last Story.
  4. Here we see 3 Stories flagged and the Epic is In Progress. Are these blockers in the current sprint or blocks that need to be cleared before the next sprint is planned?
  5. This Epics has 17 work items are Well Formed. This is great but is also means there is 1 needing some attention. Well Formed is a concept created specifically for this view. Well Formed means that there is a description, summary, acceptance criteria or steps to reproduce (both custom field in this project), and a size.
  6. Why are these 3 Stories in progress? There is plenty of work ranked higher that is ready. There could be many reasons but understanding why is important.
  7. Having 18 work items In Progress is a number the team is probably tracking as a part of their normal sprint stats. Knowing the history of the team I would be surprised if they complete 10 per sprint. This is a good place to point out that these stats are counts. I avoided working with story points because many Stories have yet to be sized and this team sizes Bugs as 0 story points.
  8. What we see here is work being completed out of rank order. Just like with the counts of In Progress being out of rank order, there also could be a valid explanation.



## Main Discovery

The big takeaway is that we were working on Epics out of rank order. Occasionally for a valid reason Epics will move and the associated work will need to adjust. But in our case, work was partially completed across the board and not being released or utilized. Also, the number of Epics that had work in progress pointed out that we were spending a large amount of time context switching between Epics trying to make as many people happy as possible. 

## Wrap Up

New insights can be discovered simply by viewing your backlog from a different perspective. In my case, looking at the status of Epics in Epic rank order turned out to be very educational. You can take a look at the Python code used to generate the stats on GitHub: https://github.com/ronjohn4/JIRAintegrations
