# Redgate's Tech Radar

The [Tech Radar](https://techradar.red-gate.com) describes the technology landscape through a Redgate lens. We've made this repo public partly because it helps us use the technology that generates the radar, and partly because it's interesting to see the technology we use at Redgate.

Policy is not captured on the radar, instead please refer to our [internal wiki](https://info.red-gate.com/display/PD/Policies).

If you're going to build a new product, the Tech Radar gives you an idea of our default favoured stack. It is intended to apply to Redgate's actively developed products. We're not making any statements about retiring any technology (though teams are encouraged to regularly have these discussions!).

The [Tech Radar](https://techradar.red-gate.com) describes the technology landscape through a Redgate lens.  We capture technology in one of four categories:
* Languages and Frameworks. Languages and frameworks that we use when building products.
* Tools. These can be components, such as databases, software development tools, such as versions control systems; or more generic categories of tools, such as the notion of polyglot persistence.
* Platforms. Things that we build software on top of such as .NET, SQL Server, Windows (etc).
* Techniques. These include elements of a software development process, such as experience design; and structuring software, such as microservices.

Items on the Tech Radar should only be captured if the cost of change is high or the benefits of standardizing outweigh the drawbacks. Each item on the tech radar should be there for the the good of Redgate or our customers. 

We are not producing a tech radar for the general tech community to consume, the tech radar is to guide our teams to build better software, so favour things that are going to be actioned over theoretical "this could be useful".

Each technology choice is positioned in one of four areas.
* **Adopt** – The technology/technique is recommended for use by the majority of teams. Consider it the default choice for new work.
  * People have the resources they need to adopt this. 
  * Where applicable, guidance is available on how to migrate from an existing technology.
* **Trial** – The technology/technique has been assessed and has clear benefits. To move something into "Trial": 
  * At least one team has plans to adopt this on a project that can support the risk.
  * Answer: "What would make us move this to Adopt?"
* **Assess** – The technology/technique has the potential to be valuable. To get something into "Assess":
  * Provide a compelling reason to assess the technology
  * Ideally, have plans for how to evaluate it in a reasonable time frame. 
  * Answer: "What would make us decide to move this to trial?"
* **Hold** - We don't want to invest effort in this technology:
  * New projects should not use this technology.
  * Currently maintained projects need to evaluate migrating to a better solution (it is accepted that this may not be feasible).

The items in the Tech Radar apply to all products in the Growth category. The Tech Radar doesn't provide all the answers, but it should give strong direction in those areas where choice makes a difference. For example, should we be favouring containers over Virtual Machines? What technology (Hyper-V vs VMWare)? Are we adopting TypeScript?

We're following Thoughtworks approach. For discussion on the quadrants, please see the [Thoughtworks Radar Faq](https://www.thoughtworks.com/radar/faq)

## What isn't on the Tech Radar?
We only use the Tech Radar to capture decisions relevant to our growth products (those that we are investing in for the future). We don't use the Tech Radar to capture historical decisions that are no longer relevant. For example, we'd prefer to say the technology we use going forward rather than listing all failed attempts in the past.

We don't include libraries on the radar. For example, it's of negligible benefit to have a standardized library for dealing with date/time or for retrieving from a URL. However, it is beneficial to standardize libraries for sharing information between services. For example, if we produce a CSV file and two libraries have different escaping conventions; that might be a problem (obviously you'd hope the spec would cover it!). Similarly, if the choice of a library makes adoption of a recommend item harder then we'll try and signpost that (for example using `Rhino.Mocks` blocks moving to `.NET 6`). We'll capture these libraries as recommendations on the internal wiki.

Examples of things that probably SHOULD NOT be on the tech radar
* RavenDB – it's not a choice anyone is going to hit in the future
* Inno Setup – Backup isn't a growth product
* Agile techniques – again, we don't believe in one correct way and capturing a list of techniques that do/do not work isn't worth it

Examples of things that probably SHOULD be on the tech radar
* .NET 8 (makes our products more aligned)
* ASP.NET Core (specific version)
* Platform technologies (it's what we should be aligning towards)
* More opinionated UI technology (React)
* Hyper-V vs VMWare equivalent (affects installation and so on)

## Who builds the radar?

The radar is open for anyone within Redgate to contribute. Before contributing please read the [Contributing Guidelines](.github/CONTRIBUTING.md).

The recommended way to propose a change or spark a discussion is to open a PR. Contributions should be promptly reviewed by the Lead Software Engineers (shout in #lead-software-engineers if this isn't the case). Comments from all other interested parties are more than welcome.

## How is the radar built?

We use the [AOE Technology Radar](https://github.com/AOEpeople/aoe_technology_radar) static site generator to build our Tech Radar. The radar is built from markdown files organized by release date.

You can see the latest version at [techradar.red-gate.com](http://techradar.red-gate.com).

The audience for this is all technical development at Redgate. It's purpose is to help us to align our technical software/practices to build greater consistency at Redgate. 

The radar is less appropriate for early stage products where we are still finding product/market fit (the concerns are less likely to be technical at this stage) though we still recommend it as a good set of default options. Our intention is that products we commit to develop/sell adhere to the tech stack in this radar.

## Building and Testing Locally

### Prerequisites
- Node.js (v16 or higher)
- npm

### Building the Radar

1. Clone the repository:
   ```bash
   git clone https://github.com/red-gate/Tech-Radar.git
   cd Tech-Radar
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Build the static site:
   ```bash
   npm run build
   ```
   This will generate the static site in the `build/` directory.

### Testing Locally

To run a local development server:
```bash
npm run serve
```

Then open your browser to [http://localhost:3000/techradar](http://localhost:3000/techradar)

## How to Contribute

### Adding or Updating Technologies

1. Create a new markdown file in the `radar/YYYY-MM-DD/` directory (create a new date folder for new releases)
2. Use the following format for your markdown file:

```markdown
---
title: "Technology Name"
ring: adopt|trial|assess|hold
quadrant: languages-and-frameworks|tools|platforms|techniques
tags: [tag1, tag2, tag3]
---

Description of the technology and why it's positioned where it is.
```

### File Naming Convention
- Use lowercase with underscores for the filename
- Example: `typescript.md`, `github_actions.md`, `docker.md`

### Quadrants
- `languages-and-frameworks`: Programming languages, frameworks, and libraries
- `tools`: Development tools, IDEs, and CI/CD systems
- `platforms`: Platform technologies including cloud, containers, and databases
- `techniques`: Development techniques, patterns, and practices

### Creating a New Release

1. Create a new folder under `radar/` with today's date in `YYYY-MM-DD` format
2. Add or copy markdown files for technologies
3. Build and test locally
4. Submit a PR

## Frequently Asked Questions

### How do I contribute?
Make a PR and it'll start a conversation in [#peergroup-lse](https://redgate.slack.com/archives/CN39BHZUK) channel!

### How do I add a new technology?
Create a new markdown file in the latest radar release folder following the format above.

### How do I move a technology to a different ring?
Copy the file to a new release folder and update the `ring` field in the front matter.
