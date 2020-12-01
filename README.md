# tellurium-nanohub-base
Baseline files needed for deploying a tellurium tool on nanoHUB

## Steps

1. Fork / Copy this repo (your nanoHUB tool's source will live in github)
1. Replace the tellurium.ipynb by your notebook (not having spaces in the notebook name is more than a good idea)
1. in middleware/invoke replace ```/usr/bin/invoke_app "$@" -C "start_jupyter -T @tool tellurium.ipynb"``` with ```/usr/bin/invoke_app "$@" -C "start_jupyter -T @tool <YOUR NOTEBOOK NAME>.ipynb"```
1. Make sure middleware/invoke has execution permition (open it in github, it'll say on the upper left), if it doesn't issue the command ```git update-index --chmod=+x middleware/invoke```
1. Follow the steps in https://nanohub.org/tools/create
