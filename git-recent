#!/bin/sh

BPURPLE='\033[1;35m'      # Purple

echo "${BPURPLE}# Recent Branches";
git for-each-ref \
      --sort=-committerdate refs/heads/ \
      --format='%(HEAD) %(color:red)%(objectname:short)%(color:reset) %(color:yellow)%(refname:short)%(color:reset) - %(contents:subject) - %(authorname) (%(color:green)%(committerdate:relative)%(color:reset))'
