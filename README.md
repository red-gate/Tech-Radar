# Tech-Radar

A [Tech Radar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar.csv) for Redgate. This helps us by recognizing the technology that:
* We use
* We're trialing and building experience
* We're excited about!
* We used to use and use no longer.

We've made this repo public partly because it helps us use the technology that generates the radar, and partly because it's interesting to see the technology and practices that we use at Redgate.

We use [Thoughtworks Tech Radar](https://radar.thoughtworks.com/) to generate our Tech Radar. The radar is backed by a single CSV file (that should nicely [render](https://help.github.com/articles/rendering-csv-and-tsv-data/)). CSV files are parsed using `d3.js` so please see their [documentation](https://d3-wiki.readthedocs.io/zh_CN/master/CSV/) for escaping rules. All changes to the Tech Radar should be completed via a PR and merged by someone else.

You can see the [latest version online](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar.csv).

The audience for this is all technical development at Redgate. It's purpose is to help us to align our technical software/practices to build greater consistency at Redgate. 

The radar is less appropriate for early stage products where we are still finding product/market fit (the concerns are less likely to be technical at this stage) though we still recommend it as a good set of default options. Our intention is that products we commit to develop/sell do adhere to the tech stack in this radar.

## Quadrants

The quadrants help us organize the entries on the Radar. We've adopted exactly the same quadrants as Thoughtworks (see their [FAQ](https://www.thoughtworks.com/radar/faq))

* *Programming Languages and Frameworks*. This was just languages but we rolled frameworks into here with the October 2012 Radar.
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
