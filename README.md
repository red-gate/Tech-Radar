# Redgate's Tech Radar

The [Tech Radar](https://techradar.red-gate.com) describes the technology landscape through a Redgate lens. We've made this repo public partly because it helps us use the technology that generates the radar, and partly because it's interesting to see the technology we use at Redgate.

Policy is not captured on the radar, instead please refer to our [internal wiki](https://info.red-gate.com/display/PD/Development+policies).

If you're going to build a new product, the Tech Radar gives you an idea of our default favoured stack. It is intended to apply to Redgate's actively developed products. We're not making any statements about retiring any technology (though teams are encouraged to regularly have these discussions!).

This version of the radar follows Thoughtworks approach. For discussion on the quadrants, please see the [Thoughtworks Radar Faq](https://www.thoughtworks.com/)

## Who builds the radar?

The radar is open for anyone within Redgate to contribute. Before contributing please read the [Contributing Guidelines](.github/CONTRIBUTING.md).

The recommended way to propose a change or spark a discussion is to open a PR. Contributions should be promptly reviewed by the Lead Software Engineers (shout in #lead-software-engineers if this isn't the case). Comments from all other interested parties are more than welcome.

## How is the radar built?

We use [Thoughtworks Tech Radar](https://radar.thoughtworks.com/) to generate our Tech Radar. The radar is backed by a single CSV file (that should nicely [render](https://help.github.com/articles/rendering-csv-and-tsv-data/)). CSV files are parsed using `d3.js` so please see their [documentation](https://d3-wiki.readthedocs.io/zh_CN/latest/CSV) for escaping rules. All changes to the Tech Radar should be completed via a PR and merged by someone else.

You can see the latest version at [techradar.red-gate.com](http://techradar.red-gate.com).

The audience for this is all technical development at Redgate. It's purpose is to help us to align our technical software/practices to build greater consistency at Redgate. 

The radar is less appropriate for early stage products where we are still finding product/market fit (the concerns are less likely to be technical at this stage) though we still recommend it as a good set of default options. Our intention is that products we commit to develop/sell adhere to the tech stack in this radar.

## Frequently Asked Questions

### It won't display properly. Help!

Common causes of this happening are:
* Leaving blank lines at the bottom (make sure these are removed)
* Forgetting to add a column (verify this by viewing it in GitHub's CSV display)
* Bad escaping
