---

## Description

This repository contains a crewAI application for generating LinkedIn posts automatically.
The crew consists of [three agents](agents.py):

1️⃣ LinkedIn Scraper

It uses a [Selenium custom tool](tools%2Flinkedin.py) to scrape my LinkedIn profile. I need to scrape my
posts since I want some examples for the last agent to emulate my writing style. This tool needs some env variables,
defined in an `.env` file (you can see an example [here](.env.example)).

2️⃣ Web Researcher

It fetches relevant information about a given topic. In my case, I chose the recent release of Llama3 by Meta AI, but
you can choose whatever you want (you'll need to modify the Tasks and Agents of course ...)

3️⃣ Influencer Agent

This agent has to deal with the information gathered by the two previous agents and write a high quality and engaging
LinkedIn post emulating my writing style.

## Usage

First of all, install the necessary dependencies.

```shell
pip install -r requirements.txt
```

After all the dependencies are installed, run the `main.py`.

> Keep in mind that you need to have all the necessary env variables in your `.env` file for this to work. Also, if you
> want to change the topic of your LinkedIn post, you'll need to modify the Agents and Tasks.

```shell
python3 main.py
```
