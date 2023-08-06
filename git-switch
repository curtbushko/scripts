#!/bin/bash

git fetch
git switch $(git branch -a --sort=-committerdate | fzf --border-label="| Git Checkout |" --border=rounded --margin=50,5,5,2)
