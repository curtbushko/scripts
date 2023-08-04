#!/bin/bash
# 	OWNER=$(gh repo view --json owner --jq .owner.login)
# 	echo "Owner: $OWNER"
# 	REPO=$(gh repo view --json name --jq .name)
# 	echo "Repo: $REPO"
_pr-review() {
	PR=$(
		GH_FORCE_TTY=100% gh pr list -s open -S user-review-requested:@me |
			fzf --ansi --preview 'GH_FORCE_TTY=100% gh pr view {1}' \
				--bind "j:down,k:up,ctrl-j:preview-down,ctrl-k:preview-up,ctrl-f:preview-page-down,ctrl-b:preview-page-up,q:abort" \
				--preview-window=top:80% --header-lines 3 |
			awk '{print $1}'
	)

	if [ -z "${PR}" ]; then
		exit 0
	fi

	PR=${PR:1}
	echo "[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] PR: ${PR}"
	BRANCH=$(gh pr view ${PR} --json headRefName --jq .headRefName)
	echo "[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Branch: ${BRANCH}"

	mkdir -p reviews
	git worktree add "reviews/${BRANCH}" -b "${BRANCH}" "origin/${BRANCH}"

	echo "[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Worktrees:"
	git worktree list
}

_pr-review "$@"
