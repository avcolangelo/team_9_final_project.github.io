Report
================
11/19/2019

## Group members (names and unis)

Alexis Colangelo, avc2129; Dania Jafar, dj2536; Si Li, sl4657; Kristal
Quispe, kq2127; Barik Rajpal, bsr2136

The written report produced by your team is central to this project.
This will detail how you completed your project, and should cover data
collection and cleaning, exploratory analyses, alternative strategies,
descriptions of approaches, and a discussion of results. We anticipate
that your project will change somewhat over time; these changes and the
reasons for them should be documented\! You will write one report
document per group, and be sure to include all group member names in the
document.

Your report should include the following topics. Depending on your
project type the amount of discussion you devote to each of them will
vary:

  - Motivation: Provide an overview of the project goals and motivation.

The motivation for our project was to create a sort of guide for
Squirral Watchers in NYC. Birdwatching is a commonon hobby and there are
many books, websites and resources surrounding this hobby. Unfortunalty
squirral watching is not as popular and is mostly only active on college
campuses. To bring more attention to this hobby, and to increase the
number of squirral watchers in NYC we created our website to serve as a
resource for the Squirral watching community in NYC. We wanted to help
this community identify where one could watch certain squirral behaviors
(i.e. foraging and climbing), squirral sounds (i.e.kuks and quaas), and
identify if there was a pattern in where one could expect different
interactions between squirral and humans (i.e. the squirral approaches
humans or is indifferent) Since alot of tourists visit NYC, we focused
on Squirral watching in Central Park.

  - Related work: Anything that inspired you, such as a paper, a web
    site, or something we discussed in class.

The following
website:<https://www.prospectpark.org/visit-the-park/things-to-do/birdwatching/?gclid=EAIaIQobChMImM7nuKaa5gIViZOzCh1NYAGQEAAYASAAEgLlPPD_BwE>
is a resource platform for birdwatching in Prospect Park that inspired
some of the work and resources we included in our project. The Prospect
park website shows a map with some of the best birding locations, our
maps similarly try to identify where certain squirral behaviours can be
obserbed.

  - Initial questions: What questions are you trying to answer? How did
    these questions evolve over the course of the project? What new
    questions did you consider in the course of your analysis?:

– What is the probability of a certain squirrel in a certain area;
visualize this probability/heat map. This questions turned into a
question of where ceratin behaviors had been, and thus could potentially
be obserbed.

– regression question: number (count) of squirrels seen eating as
predicted by foraging. Can time of day be predicted by squiral
behaviors. Different number of covariates were tested and one model won
out. The prediction of the model as a whole was not good. better
prediction, if squiral was tracked all day.

– Where are squirrels are most concentrated? This question went as we
switched directions from concentration of squirals to behaviours.

– What are the most common squirrel behaviors? Foraging is the most
common observed behavior.

  - Data: Source, scraping method, cleaning, etc.

  - Exploratory analysis: Visualizations, summaries, and exploratory
    statistical analyses. Justify the steps you took, and show any major
    changes to your ideas.

When looking at the most common squirrel behaviors, we removed the
category of “other activities” from analysis because the range of
entries varied too widely (which would make it difficult to visualize
effectively) and would be very time consuming to wrangle. Instead, we
decided to focus on the five main categories of behaviors. When looking
at the primary fur color of squirrels, 55 squirrels had missing data for
fur color, so to simplify the visualization we decided to remove the
missing data.

  - Additional analysis: If you undertake formal statistical analyses,
    describe these in detail Discussion: What were your findings? Are
    they what you expect? What insights into the data can you make? As
    this will be your only chance to describe your project in detail,
    make sure that your report is a standalone document that fully
    describes your process and results. We also expect you to write
    high-quality code that is understandable to an outside reader.
    Coding collaboratively and actively reviewing code within the team
    will help with this
