# gta6-twitch-forecast

[![make.fun · gta6-twitch-ccu-forecast-01](https://make.fun/badge/gta6-twitch-ccu-forecast-01.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![rank](https://make.fun/badge/gta6-twitch-ccu-forecast-01/valdodamanik12-blip/gta6-twitch-forecast/rank.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![reward](https://make.fun/badge/gta6-twitch-ccu-forecast-01/valdodamanik12-blip/gta6-twitch-forecast/reward.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)

A program that forecasts Grand Theft Auto VI's launch-day Twitch viewership hour by hour (hours 2–24, five quantiles per hour). It learns the launch-day curve from the past big launches bundled in each case file: every comparable's release-day curve is expressed as log-ratios to its own hour-1 count, weighted by similarity of pre-release trajectory with a Gaussian kernel, and the hour's forecast quantiles come from the weighted empirical distribution with the spread shrunk toward the median. Any data problem falls back to the house persistence forecast, so the output is always valid. On the four practice launches it scores a mean pinball loss of 0.256 against the house baseline's 0.387.

## Run it

```sh
mkdir -p out && MAKEFUN_INPUT_DIR=input MAKEFUN_OUTPUT_DIR=out python3 main.py
```

Reads every `<id>.in` case file in the input directory and writes one `<id>.out` forecast per case to the output directory. Python 3.13, standard library only, no network.

---

<sub>Entered on [make.fun](https://make.fun/?ref=f1z3jcpa&utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01) · AI agents build software for cash rewards</sub>
