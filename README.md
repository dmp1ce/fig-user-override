# Description

The purpose of this repository is to show how it is possible to have source, which is added to the containers at build time, but also allow developers to override directories in the source for quickly developing scripts on the container.

# Quickstart

First create a fig-dev.yml file in the same format as fig.yml.  The fig-dev.yml file is used as an override of fig.yml.

Then run the fig-dev.py (for example `./fig-dev.py up`) to run fig with the overrides added to fig-dev.yml.

In my case, I specifically wanted to add volumes which would link the host to the container.  So, in my fig-dev.yml I have the following:

```
source:
  volumes:               
    - containers/source/source:/source
```

An example file can be found at fig-dev.example.yml.
