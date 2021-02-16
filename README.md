# Redgate's Tech Radar

The [Tech Radar] describes the technology landscape through a Redgate lens. We've made this repo public partly because it helps us use the technology that generates the radar, and partly because it's interesting to see the technology we use at Redgate.

Policy is not captured on the radar, instead please refer to our [internal wiki](https://info.red-gate.com/display/PD/Development+policies).

If you're going to build a new product, the Tech Radar gives you an idea of our default favoured stack. It is intended to apply to Redgate's actively developed products. We're not making any statements about retiring any technology (though teams are encouraged to regularly have these discussions!).

The [Tech Radar](https://techradar.red-gate.com) describes the technology landscape through a Redgate lens.  We capture technology in one of four categories:
* Languages and Frameworks. Languages and frameworks that we use when building products.
* Tools. These can be components, such as databases, software development tools, such as versions control systems; or more generic categories of tools, such as the notion of polyglot persistence.
* Platforms. Things that we build software on top of such as .NET, SQL Server, Windows (etc).
* Techniques. These include elements of a software development process, such as experience design; and structuring software, such as microservices.

Items on the Tech Radar should only be captured if the cost of change is high or the benefits of standardizing outweigh are for the good of Redgate or our customers.
Each technology choice is positioned in one of four areas.
* Adopt – We feel strongly that Redgate should be adopting these items. It’s the default choice.
* Trial – Worth pursuing. It’s important to understand how to build up this capability. Redgate teams can try this technology on a project that can support the risk.
* Assess – Worth exploring with the goal of understanding how it will affect Redgate
* Hold - Proceed with caution

The items in the Tech Radar apply to all products in the Growth category. The Tech Radar doesn’t provide all the answers, but it should give strong direction in those areas where choice makes a difference. For example, should we be favouring containers over Virtual Machines? What technology (Hyper-V vs VMWare)? Are we adopting TypeScript?

We're following Thoughtworks approach. For discussion on the quadrants, please see the [Thoughtworks Radar Faq](https://www.thoughtworks.com/radar/faq)

## What isn’t on the Tech Radar?
We only use the Tech Radar to capture decisions relevant to our growth products (those that we are investing in for the future). We don’t use the Tech Radar to capture historical decisions that are no longer relevant. For example, we’d prefer to say the technology we use going forward rather than listing all failed attempts in the past.

Examples of things that probably SHOULD NOT be on the tech radar
* RavenDB – it’s not a choice anyone is going to hit in the future
* Inno Setup – Backup isn’t a growth product
* Agile techniques – again, we don’t believe in one correct way and capturing a list of techniques that do/do not work isn’t worth it

Examples of things that probably SHOULD be on the tech radar
* .NET 5 (makes our products more aligned)
* ASP.NET Core (specific version)
* Platform technologies (it’s what we should be aligning towards)
* More opinionated UI technology (React)
* Hyper-V vs VMWare equivalent (affects installation and so on)

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
