#!/bin/bash

SEARCH_QUERY='jira issue list -a$(jira me) --plain --columns id,summary,status' 
FZF_DEFAULT_COMMAND=$SEARCH_QUERY fzf \
  --preview-window=top,60%,border-sharp \
  --reverse \
  --border=none \
  --preview-label='PREVIEW' \
  --bind "j:down,k:up,q:abort" \
  --bind 'e:execute(jira issue edit {1})'\
  --bind 'm:execute(jira issue move {1})' \
  --preview='jira issue view {1}'
