#!/bin/bash

fd() {
  preview="git diff $@ --color=always -- {-1}"
  git diff "$@" --name-only | fzf --preview-window=top:80% --bind "j:down,k:up,q:abort" -m --ansi --preview "$preview"
}

fd "$@"
