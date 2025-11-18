# Göteborgdle [WIP]

> Göteborgdle is an unnoficial game and is not associated with Västtrafik

Göteborgdle is a Wordle-style game where you have to guess the daily stop of the Gothenburg tram. The project is developed by a group of friends from Gothenburg 💙

The project is under active development, for any feature suggestions, bug reports, or collaborations, reach out to us at info@goteborgdle.se

If you want to help Göteborgdle stay alive, you can get us a fika 🫶

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/V7V81OME3W)

## For developers
### Our CI
In both the front- and back-end repositories we follow similar CI structure. We have 2 pipelines in both: **Test** and **Deploy**. 

The **test** pipeline has some unit tests on the backend and some Jest tests for the frontend (_most of them are vibecoded_ but essential for seeing that the system runs before deploying it) we try to keep the tests up to date with the code. Tests run on each push, as well as on PRs.

The **deploy** pipelines are a bit more tricky. They have 2 stages, the 1st one checks that there was a test pipeline that passed on the same commit. Then a temporary runner is created in our Tailscale (VPN) network that opens an ssh to our deploy server. Afterwards, the pipeline checks out on the commit and runs the deploy script.

**To deploy new changes to prod**, make sure the required changes are in the main branch, then create a new release (and a tag), the tag has to be named as follows: vx.x.x, following the semantic versioning. Then check that the deploy pipeline succeeds in the "Actions" tab.

For questions and support with CI contact [pronoooobster](https://github.com/pronoooobster)
<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
