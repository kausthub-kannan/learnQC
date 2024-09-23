---
layout: post
title: Contributing to the Project
permalink: /CONTRIBUTING/
---

# CONTRIBUTING
Thanks for contributing to learnQC and to expand the niche community of Quantum Computing (QC). Please follow the below instaructions to setup jenkyll to locally run the website and follow the guidelines for uniformity 😁🫡

## Setup
Here is how you can setup locally to test your contributions:

#### Linux / MacOS
The current docs is for debain based package manager, use equivalent package manager to install the dependecies.

**Setup ruby and gem:**
```bash
sudo apt-get update
sudo apt-get install ruby-full
export PATH="/usr/local/opt/ruby/bin:$PATH"
source ~/.bash_profile
```

**Setup jenkyll and the project:**
```bash
sudo gem install jekyll bundler
```

Navigate to the project directory and run the below command:
```bash
bundle install
bundle exec jekyll build
bundle exec jekyll serve
```

## Guidelines
- It is prefered you use Obisidan for editing the docs which could optimise the contribution.
- When creating a new webpage, add it to appropriate folder (ex: all algorithms should be added to _algorithms folder)
- For every new webpage add the below at the begining of the page:

```
---
layout: post
title: Name to appear at the side bar
permalink: /path_on_the_bar/ **Note:** Use % to add spaces
---
```

- If a new subsection needs to be created, create a folder with the name of subsection with '_' in the start of the name and add the folder with title in _config.yml
