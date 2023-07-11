#!/bin/bash

gstat() {
	DAYS=$1
	COUNT=$2
	FROM=$(date -v-${DAYS}d +"%d %h, %Y")
	TO=$(date +"%d %h, %Y")

	echo "Top ${COUNT}, last ${DAYS} days: (from ${FROM} to ${TO})"
	git shortlog -sn --no-merges --since="${FROM}" --before="${TO}" | grep -v 'bot' | head -${COUNT}
}

gstat "7" "5"
gstat "14" "10"
gstat "30" "10"
gstat "60" "10"
gstat "90" "10"
gstat "180" "10"
gstat "365" "20"
