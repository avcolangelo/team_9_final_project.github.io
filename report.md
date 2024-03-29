Report
================
11/19/2019

The written report produced by your team is central to this project.
This will detail how you completed your project, and should cover data
collection and cleaning, exploratory analyses, alternative strategies,
descriptions of approaches, and a discussion of results. We anticipate
that your project will change somewhat over time; these changes and the
reasons for them should be documented\! You will write one report
document per group, and be sure to include all group member names in the
document.

**Group members (names and unis)** Alexis Colangelo, avc2129; Dania
Jafar, dj2536; Si Li, sl4657; Kristal Quispe, kq2127; Barik Rajpal,
bsr2136

## Motivation:

The motivation for our project was to create a sort of guide for
Squirrel Watchers in NYC. Birdwatching is a common hobby and there are
many books, websites and resources surrounding it. Unfortunately
squirrel watching is not as popular and is mostly only active on college
campuses. To bring more attention to this hobby, and to increase the
number of squirrel watchers in NYC, we created our website to serve as a
resource for the squirrel watching community in NYC. We wanted to help
this community identify where one could watch certain squirrel behaviors
(i.e. foraging and climbing), hear squirrel sounds (i.e. kuks and
quaas), and identify if there was a pattern in where one could expect
different interactions between squirrels and humans (i.e. the squirrel
approaches humans or is indifferent) Since a lot of tourists visit NYC,
we focused on Squirrel watching in Central Park.

## Related work:

The following
website:<https://www.prospectpark.org/visit-the-park/things-to-do/birdwatching/?gclid=EAIaIQobChMImM7nuKaa5gIViZOzCh1NYAGQEAAYASAAEgLlPPD_BwE>
is a resource platform for birdwatching in Prospect Park that inspired
some of the work and resources we included in our project. The Prospect
park website shows a map with some of the best birding locations, our
maps similarly try to identify where certain squirrel behaviors can be
observed.

## Initial questions:

Some of our questions and their evolution are below:

1.  What is the probability of a certain squirrel in a certain area;
    visualize this probability/heat map.

This question turned into a question of where certain behaviors had
already been observed, and thus where a behavior could potentially be
observed again.

2.  Regression question: number (count) of squirrels seen eating as
    predicted by foraging.

This question evolved into whether certain squirrel behaviors could
predict the time of the day (AM or PM) in which the squirrel was
observed. Different number of covariates were tested and one model won
out. The prediction of the model as a whole was not good. But the model
could be improved potentially if individual squirrels were tracked all
day as opposed to tracking observations of different squirrel
appearances.

3.  Where are squirrels are most concentrated?

We decided not to pursue this question as our general direction switched
from being where most squirrels could be observed to how we could use
squirral behaviors to predict time of day for squirrel sightings.

4.  What are the most common squirrel behaviors?

From our analysis of behavior foraging is the most common squirrel
behavior.

## Data:

For our project we used the 2018 Central Park Squirrel Data from NYC
Open Data. Over all the data set did not include much missing data, but
in the event that a particular variable was under analysis with missing
data we dropped the rows with missing data.

For our Squirrel Behavior maps we imported the data and filtered the
data to only include behaviors. We recoded the behavior variables
(running, chasing, climbing, eating, foraging, tail flags and tail
twitches into factor and then integer variables. To create three
different maps, we filtered the data and created three different mini
data sets (behavior\_data, sound\_data, and interact\_data). We then
used leaflet to plot the maps of the behaviors.

For our Common Behaviors analysis, we imported the data and re-coded the
behaviors (running, chasing, climbing, eating and foraging) as factor
variables. We then recoded the behaviors from TRUE/FALSE to No and the
associated behavior (i.e. for running, FALSE was recoded to No, and TRUE
was recoded to running). We then tidied the data and used pivot longer
to capture all behaviors in one column (activity).

For our Logistic regression analysis, we imported the data but not very
much data cleaning was necessary, as all the squirrel behaviors were
already coded as TRUE or FALSE and had no missing values. We did create
a new variable to use as an ID variable to help split the data into
training and testing sets. We also recoded the AM and PM response
variable to be 0 or 1 (1 for AM). We let the step function create 1
logistic regression model, and then removed a few of the less
significant covariates to create a model with better parsimony.

## Exploratory analysis:

When looking at the squirrel behavior maps…

When looking at the most common squirrel behaviors, we removed the
category of “other activities” from analysis because the range of
entries varied too widely (which would make it difficult to visualize
effectively) and would be very time consuming to wrangle. Instead, we
decided to focus on the five main categories of behaviors. When looking
at the primary fur color of squirrels, 55 squirrels had missing data for
fur color, so to simplify the visualization we decided to remove the
missing data.

## Additional analysis:

#### Logistic regression

**Motivation:**

Our motivation for this analysis was to try to use statistical
techniques to analyze associations between various squirrel behaviors.
We began by considering if any specific squirrel behavior could be
modeled by the other squirrel behaviors. However, while thinking about
the squirrel behaviors, we found ourselves wondering if any were
associated with time of day, and that evolved into us deciding to use
logistic regression models to see if we could accurately predict the
time of day an observation was recorded (AM vs PM) using the squirrel
behaviors observed.

**Results:**

The results of our logistic regression models suggest that many of the
squirrel behaviors, such as eating, climbing, approaches, and
indifferent are associated with a time of day. Eating is more strongly
associated with PM, while climbing, approaches, and indifferent
behaviors are more associated with AM. However, in using our models to
create predictions, we found that the accuracy of both models was below
60%, which is quite poor\! After examining the squirrel behaviors
further, we noted that the observations had a median of 2 different
squirrel behaviors per observation (out of 13 total), and so that could
be a reason for the low predictive power. If the squirrels were observed
for longer, and had more behaviors included per observation, it is
possible we would have a logistic regression model with better
predictive power.

## Discussion:

From our data set we found that there were 3023 unique squirrels
observed in Central Park in October of 2019. The three types of fur
color observed were grey, cinnamon, and black with Grey Squirrel’s being
the most observed type of colored squirrel. In regards to behavior,
foraging was the most prominent behavior observed and chasing was the
least common behavior observed. We didn’t really have much of a
background in Squirrel behaviors and characteristics, but since the data
was collected in the fall, we expected that squirrels would be mostly
foraging since they are less active in the winter time. After some
investigation we found that tree squirrels, like the Eastern Gray and
American Red Squirrel, do not hibernate, but they do tend to sleep a lot
during the winter months. We also found that squirrels usually live
through the winter by putting their food in shallow holes for storage to
serve as a food reserve in the winter and that throughout the fall, they
maximize food consumption and body mass. Thus, our behavior analysis
results line up with the behavior trends we found online. Overall the
data was easy to work with since there was not much cleaning necessary,
but it was limited in its predictive abilities and in its abilities to
give information on squirrel behavior outside of the month of October
and thus outside of the Fall season.
