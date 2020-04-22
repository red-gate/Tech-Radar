# Redgate's Tech Radar

The [Tech Radar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar.csv) describes the technology landscape through a Redgate lens. We've made this repo public partly because it helps us use the technology that generates the radar, and partly because it's interesting to see the technology we use at Redgate.

Items on the tech radar are only captured if the cost of change is high, or the benefits of standardizing are for the good of Redgate or our customers.

Policy is not captured on the radar, instead please refer to our [internal wiki](https://info.red-gate.com/display/PD/Development+policies).

Items are placed into one of four categories.

* Languages and Frameworks. Languages and frameworks that we use when building products.
* Tools. These can be components, such as databases, software development tools, such as versions control systems; or more generic categories of tools, such as the notion of polyglot persistence.
* Platforms. Things that we build software on top of such as .NET, SQL Server, Windows (etc).
* Techniques. These include elements of a software development process, such as experience design; and ways of structuring software, such as microservices.

For each item, we position it in one of four states:

* Adopt – This technology should be the default choice in a technology area
* Explore – Technology we’re interested in but need to evaluate before recommending as the default choice. Items in this category should have a team willing to sponsor the exploration.
* Endure – We’ve used this technology in the past, but it’s no longer recommended.
* Retire - This technology is holding us back and should be actively removed. Items in this category should have a desired removal date.

The radar only applies to all actively developed products at Redgate. 

Items in the [primary Tech Radar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar.csv) have an expectation that it should be followed (where appropriate) for all teams at Redgate. For example, if C# X arrives then we get most benefit from adopting it wholesale across the organization, whereas a particular date/time library is a local choice for a development team. The  [Library Tech Radar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar_libraries.csv) aims to support teams with local decisions by sharing experience from other teams.

## How is the radar built?

We use [Thoughtworks Tech Radar](https://radar.thoughtworks.com/) to generate our Tech Radar. The radar is backed by a single CSV file (that should nicely [render](https://help.github.com/articles/rendering-csv-and-tsv-data/)). CSV files are parsed using `d3.js` so please see their [documentation](https://d3-wiki.readthedocs.io/zh_CN/master/CSV/) for escaping rules. All changes to the Tech Radar should be completed via a PR and merged by someone else.

You can see the latest version at [techradar.red-gate.com](http://techradar.red-gate.com).

We also have a [Library Tech Radar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fred-gate%2FTech-Radar%2Fmaster%2Fradar_libraries.csv) to give a more detailed view of specific libraries we use.

The audience for this is all technical development at Redgate. It's purpose is to help us to align our technical software/practices to build greater consistency at Redgate. 

The radar is less appropriate for early stage products where we are still finding product/market fit (the concerns are less likely to be technical at this stage) though we still recommend it as a good set of default options. Our intention is that products we commit to develop/sell adhere to the tech stack in this radar.

## Who builds the radar?

The radar is open for anyone within Redgate to contribute.

Contributions are reviewed by Redgate’s Technical Advisory Board (TAB).  The TAB consists of a group of senior technology leaders within Redgate (Lead Software Engineers, Head of IT, Head of CORE, Head of Product Engineering) and is led by the CTO.

## Frequently Asked Questions

Q. It won't display properly. Help!

A. Common causes of this happening are:
* Leaving blank lines at the bottom (make sure these are removed)
* Forgetting to add a column (verify this by viewing it in GitHub's CSV display)
* Bad escaping

Q. Do I have to include every single npm package?

A. No. That will drive you insane. If it's a "micro-library" (e.g. something with no dependencies) then it's not something that we should represent on the tech radar, if it's something you think another team might find useful eg, if you invested time spiking and investigating several alternatives, consider adding it to the Library Tech Radar.

Q. What's the difference between the Tech-Radar and Library Tech-Radar

A. `radars.csv` represents the high-level technology in use at Redgate. It includes high-level techniques, platforms, languages and frameworks that we use as well as tools. It also includes libraries where the cost of change is high (for example, Test frameworks, mocking libraries or user interface).

`radar_libraries.csv` gives a more detailed view of the libraries we use, including our npm and NuGet dependencies. The purpose of this second radar is to help teams make quicker decisions about what libraries to use by avoiding spending time investigating eg "Which drag and drop library is best for React?" when another team has already done it.

Use of libraries in this radar  should not cause knock-on dependencies but add some useful functionality that would not be worth re-inventing. As a general guideline if your library contains many dependencies that enforce choice on others it should probably be in `radar.csv`
