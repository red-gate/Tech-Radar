# Tech-Radar

A [Tech Radar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar.csv) for Redgate. This helps us by recognizing the technology that:
* We use.
* We're trialing and building experience.
* We're excited about!
* We used to use and use no longer.

We've made this repo public partly because it helps us use the technology that generates the radar, and partly because it's interesting to see the technology and practices that we use at Redgate.

We use [Thoughtworks Tech Radar](https://radar.thoughtworks.com/) to generate our Tech Radar. The radar is backed by a single CSV file (that should nicely [render](https://help.github.com/articles/rendering-csv-and-tsv-data/)). CSV files are parsed using `d3.js` so please see their [documentation](https://d3-wiki.readthedocs.io/zh_CN/master/CSV/) for escaping rules. All changes to the Tech Radar should be completed via a PR and merged by someone else.

You can see the latest version at [techradar.red-gate.com](http://techradar.red-gate.com).

We also have a [Library Tech Radar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar_libraries.csv) to give a more detailed view of specific libraries we use.

The audience for this is all technical development at Redgate. It's purpose is to help us to align our technical software/practices to build greater consistency at Redgate. 

The radar is less appropriate for early stage products where we are still finding product/market fit (the concerns are less likely to be technical at this stage) though we still recommend it as a good set of default options. Our intention is that products we commit to develop/sell do adhere to the tech stack in this radar.

## Quadrants

The quadrants help us organize the entries on the Radar. We've adopted the same quadrants as Thoughtworks (see their [FAQ](https://www.thoughtworks.com/radar/faq))

* *Languages and Frameworks*. Languages and frameworks that we use when building products.
* *Tools*. These can be components, such as databases, software development tools, such as versions control systems; or more generic categories of tools, such as the notion of polyglot persistence.
* *Platforms*. Things that we build software on top of such as .NET, SQL Server, Windows (etc).
* *Techniques*. These include elements of a software development process, such as experience design; and ways of structuring software, such as microservices.

Like Thoughtworks we don't make a big deal out of the quadrants. It just exists as a way to break up the radar.

## Rings

The rings in the quadrants help us choose the technology. The rings are:

* *Adopt* - This is the technology you should be choosing to solve a problem. Everything in here forms our default set of technology choices (for example, C#), and will already be in-use with at least one Redgate team.

* *Explore* - This has potential and is worth experimenting with in 10% time or running a trial on your team. Putting something in Explore is a commitment to explore it between now and the next issue of the Tech Radar. The description of any Explore item should state who is committed to exploring it.

* *Endure* - This is no longer how we do things. It is OK for this to be used in Product Development, but don't add more of it and migrate off it wherever possible.

* *Retire* - Don't use this technology! If you are using it then you should be spending some time migrating away from this. Examples of this would include old libraries that aren't updated with security frameworks.

## Commitment and Accountability

Following the publication of the initial tech radar, we'll review this regularly every six months.

At that time, we'll ask those using items in Explore to share their experience and make some decisions from there:
* Explore -> Adopt - Technology has proven itself and should be the new default
* Explore -> Endure - It's OK (not causing us problems) but isn't giving us any advantage over others
* Explore -> Retire - The technology or technique isn't appropriate for us
* Explore -> Explore - The technology or technique needs longer to prove itself
* Explore -> off ring - This technology wasn't explored and is no longer appropriate.

We'll look at items in Retire and (hopefully) find they can be removed from the radar because they have been retired. If the cost of removing them has proved higher than we imagined, then we can reconsider moving that thing back to Endure.

## Frequently Asked Questions

Q. Do I have to include every single npm package?

A. No. That will drive you insane. If it's a "micro-library" (e.g. something with no dependencies) then it's not something that we should represent on the tech radar, if it's something you think another team might find useful eg, if you invested time spiking and investigating several alternatives, consider adding it to the Library Tech Radar.

Q. What's the difference between the Tech-Radar and Library Tech-Radar

A. `radars.csv` represents the high-level technology in use at Redgate. It includes high-level techniques, platforms, languages and frameworks that we use as well as tools. It also includes libraries that have accomplish significant tasks where the cost of change is high (for example, Test frameworks, mocking libraries or user interface).

`radar_libraries.csv` gives a more detailed view of the libraries we use, including our npm and NuGet dependencies. The purpose of this second radar is to help teams make quicker decisions about what libraries to use by avoiding spending time investigating eg "Which drag and drop library is best for React?" when another team has already done it.

Use of libraries in this radar  should not cause knock-on dependencies but add some useful functionality that would not be worth re-inventing. As a general guideline if your library contains many dependencies that enforce choice on others it should probably be in `radar.csv`
