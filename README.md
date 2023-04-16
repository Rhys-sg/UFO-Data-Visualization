# UFO-Data-Visualization

### To use:
Click `choose file` button and then choose **ufo_sightings.csv** (from the repo).

### Credits:
Created with <a href="https://github.com/laolarou726">@laolarou726</a>

##
### Introduction
For Group Project 2: Designing with Data, we were tasked with modeling different modes of communicating with data. With our representation, we needed to covey data with two different intentions. The first was to covey the data meaningfully and clearly, while the second was to do so in a way that evokes emotions and provides an experience for the observer. Therefore, we asked ourselves, “how might we find creative ways of representing and displaying data for clarity and emotional impact?”

Before ideating design systems, we first needed to find a dataset. We chose to focus on data that we felt personally interested in. Some potential datasets were interesting because they represented a significant issue for people. An example of this dataset is the one describing cumulative cancer deaths. However, we assumed that most of the class would focus on these topics, so we instead went with datasets that we found unique. The dataset we landed on tallied descriptions of reported UFO sightings. We found little coverage of this topic, and we decided to focus on it because of its obscurity.

### Initial Steps
Before representing our data in either direction, we first needed to “clean” our data and make sense of the vast amount of information. The UFO sightings data set was a collection of over 60,000 sightings, including the location of the sighting (city, state, country, longitude, and latitude), a description of the observed UFO, the encounter duration, and when the sighting occurred. Overall, this was an incomprehensible amount of information. Our first steps were to decide what we could derive from this data and what would be meaningful to represent. Some data, such as the duration of the encounter, did not have any significant connection with other data, so we decided not to highlight them. However, the dataset did not explicitly state some of the most exciting data. These pieces of information (such as how many sightings were in a year) had to be derived using code. With over 60,000 entries, it was not feasible to distill data manually, so we opted to automate the process using Python. We used a similar method to understand correlations between frequency and state, frequency per capita of states, and shapes of UFOs over time.

### Visualizations
To visualize the dataset, we used HTML and Vega-Lite visualizations. Along with looking amazing, these had the added benefit of being interactive. As mentioned above, our visual representations aimed to convey the data meaningfully and clearly. Interactive graphics meant when portraying our complex dataset, we could partially rely on interactive graphics to portray information. The three graphs we made visualized the number of sightings over time, the number of sightings per capita in U.S. states, and the number of sightings that describe a similarly shaped UFO over time.

We used our distilled data about the number of observations per year to represent the number of UFO sightings over time. In the bar graph below, we plotted the number of observations as the y-axis and the years as the x-axis. This was our most straightforward representation and aimed to show an observer how the frequency of reports has changed over time.

![image](https://user-images.githubusercontent.com/127057159/232334582-99da4997-43f5-4696-b952-1e6a7efdb038.png)

Representing the number of UFO sightings per capita in U.S. states was considerably more complicated. Again, we used Vega-Lite and our distilled data by tallying how many sightings occurred in a given state. However, it was much harder to find a graphic that would represent this data. Before we found the example graphic, we experimented with a few prototypes to come up with a way to visualize the relationship. These were made in a Figma file and are shown below.

![image](https://user-images.githubusercontent.com/127057159/232334599-e286bfd2-63dc-4f63-85cc-d9aaf822aece.png)

After finding one of Vega-Lite’s examples, we imported our dataset and visualized the frequency per state. We realized the data only represented the population of a state. So, to account for population, we decided to represent UFO sightings per capita instead. To do this, we divided the sighting by the state’s population. Our final graph is shown below.

![image](https://user-images.githubusercontent.com/127057159/232334614-4bbcf43d-5600-40d4-a1ac-53e171b4198a.png)

Interestingly, this gave us very similar results to our initial graph. Notably, California has a skewed number of reports, showing more UFO sightings than any other state by a significant margin. Initially, we assumed this was because of California’s large population. However, after adjusting for population, it makes us wonder why the state has so many UFO sightings.

Our final visualization shows how the shape of observed UFOs has changed over time. To visualize this, we used a bar chart again to graph the quantity of a given shape per year. These are stacked on top of each other so that the graph can also show the trends in overall sightings. An image of the graph is shown below. In the interactive version, we have included a tooltip when you move the cursor on the graph. This lets users better distinguish between the shapes we represented, as so many colors appear similar.

![image](https://user-images.githubusercontent.com/127057159/232334631-0706e30b-89fa-4846-9f23-20599676e350.png)

### Visceralization
For our second task: to design a representation that would emulate an experience or force emotions from an observer, we used a visceral representation to represent how incomprehensible the number of UFO sightings is. Klein and D’Ignazio wrote about the concept and uses for data visceralizations in their book Data Feminism. According to Klein and D’Ignazio, while “visual things are for the eyes, […] visceralizations are representations of data that the whole body can experience, emotionally as well as physically” (Klein and D’Ignazio 84, 2020). We used visceralizations to show how unique each sighting is and how it does not do them justice by plotting them as a graph. To do this, we highlighted the different rates at which human senses can understand data. If shown numbers for a reasonable amount of time, humans can develop an understanding of the quantity those numbers represent. However, if given multiple auditory sources, it is significantly more challenging for humans to understand that data individually.

To compare these two senses, our visceralization visually shows the number of reported UFO sightings in a year. This stays for two seconds before being updated to the next year. An example of one slide is shown below.

![image](https://user-images.githubusercontent.com/127057159/232334647-124ad3be-b5c8-48ff-85b4-d314d8d8def5.png)

While the slide is shown to a user, the video plays “The War of the Worlds” by Orson Welles, a Halloween episode of the radio series as an adaptation of H. G. Wells’s novel The War of the Worlds. The radio station converted Wells’ 40-year-old novel into fake news bulletins describing a Martian invasion of New Jersey (Schwartz, 2015). According to the Smithsonian, “Some listeners mistook those bulletins for the real thing, and their anxious phone calls to police, newspaper offices, and radio stations convinced many journalists that the show had caused nationwide hysteria” (Schwartz, 2015). We chose to use “The War of the Worlds” as our audio not only because it was a historical event that highlighted both the U.S.’s perception of aliens but also the importance of designers’ portrayal of information. In minor cases, incorrect data portrayal confuses users, but in significant cases, it leads to unintended consequences, such as listeners of “The War of the Worlds” mistaking it for a “real” broadcast.

Using “The War of the Worlds” to represent our data, we chose to overlay multiple versions of the audio over each other. For every 100 UFO sighting in a year, a new version of “The War of the Worlds” starts to play. While the number of reports stays in the 100s to 300s, Orson Welles is difficult to understand but understandable nonetheless. However, when the number of UFO sightings spiked in the late 1990s, the number of UFO sightings and the audio becomes incomprehensible.

### Conclusion
Comparing the two methods of representing data (visual and visceral), they both have different benefits and uses. Visual representations are far better at clearly representing information. Assuming they are designed well, users can quickly and easily understand visual representations. Additionally, users do not have to interact with visual representations as much as visceral representations. The flow of knowledge is concise and one-directional. When interacting with visual representations, users often do not need to digest and consider the choices a designer made when representing that data and what the designer intended to evoke. This is not necessarily a good or bad thing.

Comparatively, visceral designs often portray more nuanced information. Designers use them when visual representations would not adequately evoke the emotions that a designer intends. In that way, visceral designs are often more aligned with fine art than visual designs. An additional benefit of visceral designs is that they require more interaction than visual designs. They make a user consider more and come to their own conclusion about the data. Therefore, they give more agency to a user to perceive the data set. Both visual and visceral designs have their place because they are used to accomplish very different goals. Visceral designs can do many things that visual can not, and vice versa. Knowing when to use either is an important skill that designers need to develop.

UFO Sightings Visceralization: https://youtu.be/ru0hb6n976w

### Work Cited

Klein, Lauren F, and Catherine D’Ignazio. Data Feminism. Cambridge, Massachusetts, The Mit Press, 2020.

Schwartz, A. Brad. “The Infamous “War of the Worlds” Radio Broadcast Was a Magnificent Fluke.” Smithsonian, Smithsonian.com, 6 May 2015, www.smithsonianmag.com/history/infamous-war-worlds-radio-broadcast-was-magnificent-fluke-180955180/.
