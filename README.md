# Tech-Radar

A Tech Radar for Redgate. This helps us by recognizing the technology that:
* We use
* We're trialing and building experience
* We're excited about!
* We used to use and use no longer.

We use [Thoughtworks Tech Radar](https://radar.thoughtworks.com/) to generate our Tech Radar. The radar is backed by a single CSV file (that should nicely [render](https://help.github.com/articles/rendering-csv-and-tsv-data/)). CSV files are parsed using `d3.js` so please see their [documentation](https://d3-wiki.readthedocs.io/zh_CN/master/CSV/) for escaping rules. All changes to the Tech Radar should be completed via a PR and merged by someone else.

You can see the [latest version online](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar.csv).

We can have [multiple radars for different contexts](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fsmaller-context.csv) if they are useful. Maybe a separate radar for desktop and server-bound tools would be useful alongside a global overview?

Please note this is public!

## Quadrants

The quadrants help us organize the entries on the Radar. We've adopted exactly the same quadrants as Thoughtworks (see their [FAQ](https://www.thoughtworks.com/radar/faq))

* *Programming Languages and Frameworks*. This was just languages but we rolled frameworks into here with the October 2012 Radar.
* *Tools*. These can be components, such as databases, software development tools, such as versions control systems; or more generic categories of tools, such as the notion of polyglot persistence.
* *Platforms*. Things that we build software on top of such as .NET, SQL Server, Windows (etc).
* *Techniques*. These include elements of a software development process, such as experience design; and ways of structuring software, such as microservices.

Like Thoughtworks we don't make a big deal out of the quadrants. It just exists as a way to break up the radar.








