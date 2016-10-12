# Hivemind

Hivemind is an experimental knowledge-management system built to help Khan Academy's Long-term Research group share intellectual context.

In the course of our research, we review lots of papers, books, games, toys, etc. We’re mining for quotes, great ideas, other promising resources, inspiration. When we find something great, that becomes part of our research team’s shared intellectual context—one of the most valuable things we build!

![Screenshot as of May 5th, 2016](screenshot.png)

Disclaimers: The project is still very young, and it's probably not useful outside of Khan Academy. It's still in a rough prototype stage, intentionally not yet robustly architected.

## Running a local server

First, [install Meteor](https://www.meteor.com/install): `curl https://install.meteor.com/ | sh`

This app requires valid credentials for Amazon S3, Google OAuth, and SMTP.

If you're at Khan Academy, copy the [secrets from Phabricator](https://phabricator.khanacademy.org/K145) into `settings.json` in the root of the project directory. If you're not, modify `settings.template.json` to use your secrets.

Run a local server with `meteor --settings settings.json`.

## Deploying to Khan Academy's Hivemind instance

(Intentionally not yet linking to the instance publicly—still evolving…)

The Long-term Research Hivemind currently runs on Heroku. Ask [Andy](mailto:andy@khanacademy.org) for push access, then:

1. [Install the Heroku toolbelt](https://toolbelt.heroku.com/).
2. Add Heroku's remote in your git checkout: `heroku git:remote -a ka-hivemind`
3. Push your branch to Heroku: `git push origin heroku`

