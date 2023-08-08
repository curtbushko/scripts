#!/bin/bash

# Run this with an alias or else the 'cd' will not work.
# Eg: alias gwts=". git-worktree-switch"

_wt-switch() {
	WT=$(
		git worktree list |
			fzf --ansi --border-label="| Worktrees |" --height=90% --border=rounded \
				--margin=2,2,2,2 --prompt "worktree: " --preview-window=top:80% \
				--preview='git log --oneline -n10 {2}' \
				--bind "j:down,k:up,ctrl-j:preview-down,ctrl-k:preview-up,ctrl-f:preview-page-down,ctrl-b:preview-page-up,q:abort" |
			awk '{print $1}'

	)
	if [ "${WT}" != "" ]; then
		cd $WT
	fi
}

_wt-switch
