#!/bin/bash
_git-worktree-add() {
	BRANCH=$1
	if [ "${BRANCH}" != "" ]; then
		echo "[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Adding Branch: ${BRANCH}"
		git worktree add "${BRANCH}" -b "${BRANCH}"
		echo "[$(date -u +'%Y-%m-%dT%H:%M:%SZ')] Worktrees:"
		git worktree list
	fi

}

_git-worktree-add "$@"
