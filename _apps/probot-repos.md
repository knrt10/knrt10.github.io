---
title: probot-repos
description: Probot extension for events that return undefined
logo:
- https://user-images.githubusercontent.com/24803604/40576469-b92c2b30-6114-11e8-87cf-eb435b2a50db.jpeg

authors:
- knrt10
stars: 6


repository: knrt10/probot-repos
githubUrl: https://github.com/knrt10/probot-repos
---

# probot-repos
Probot extension for events that return **undefined**

# What's its importance ?

Some github events like `installation` & `installation_repositories` does not work for probot's
`context.repo()` as they return **undefined** because in that case their payload does not store values for which **repository/repositories** were added. This is just a simple hack for helping developers using probot to avoid writing large amount of code. :smile: :fire:

# Installation

1.) Install using npm `npm i probot-repos --save`

# Usage

```js
const repos = require('probot-repos')
robot.on('installation.created', context => {
    repos(context).then((val) => {
      // val will return array of repositories added .
      [ { repo: 'Awesome-Hacking', owner: 'USERNAME' },
      { repo: 'autolabeler', owner: 'USERNAME' } ]
    })
})
```
Enjoy coding :peace_symbol:
