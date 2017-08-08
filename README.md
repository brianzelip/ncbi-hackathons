This is a work-in-progress for creating a [NCBI-Hackathons website](https://NCBI-Hackathons.github.io) that automatically renders the most current list of minimum viable projects shipped from NCBI Hackathons.

This small web app renders data about NCBI-Hackathons repos on the fly on the client side. It fetches data from an endpoint exposed from a [small Node app hosted on Glitch.com](https://glitch.com/edit/#!/able-viper) that queries [GitHub's graphql api](https://developer.github.com/v4/).

Changes to make on each repo that has shipped a MVP and that is to be included in the list of NCBI-Hackathons products:

- create the display title for the repo by creating an issue with:
  - the title `title`
  - the body with a single line containing the title case string of the title of the repo to be displayed in the main list (ie: no underscores, hyphens, etc)
  - apply the label `title` to the issue
- create the URL for the manuscript associated with the repo if one exists, by creating an issue with:
  - the title `manuscript`
  - the body with a single line containing the full URL to the manuscript associated with the repo to be displayed in the main list
  - apply the label `manuscript` to the issue
- make sure there is a full description at the head of the main repo page, so that this repo description can be displayed in the main list
  - if there comes a need for a more robust description than what the GitHub repo description field allows, we can handle it with an issue like `title` and `manuscript`.
