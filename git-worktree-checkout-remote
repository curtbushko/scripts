#!/bin/bash
# 	OWNER=$(gh repo view --json owner --jq .owner.login)
# 	echo "Owner: $OWNER"
# 	REPO=$(gh repo view --json name --jq .name)
# 	echo "Repo: $REPO"
_git-worktree-checkout() {
	BRANCH=$(
		git branch -r --sort=-committerdate |
			fzf --ansi --border-label="| Branches |" --height=90% --border=rounded \
				--margin=2,2,2,2 --prompt "checkout worktree: " --preview-window=top:40% \
				--preview='git log --oneline -n10 {1}' \
				--bind "j:down,k:up,ctrl-j:preview-down,ctrl-k:preview-up,ctrl-f:preview-page-down,ctrl-b:preview-page-up"
	)

	if [ "${BRANCH}" != "" ]; then
		BRANCH=$(echo ${BRANCH} | tr -d '[:space:]' | sed 's^origin\/^^g')
		echo "[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Branch: ${BRANCH}"
		git worktree add "${BRANCH}" -B "${BRANCH}" "origin/${BRANCH}"
		echo "[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Worktrees:"
		git worktree list
	fi

}

_git-worktree-checkout "$@"
