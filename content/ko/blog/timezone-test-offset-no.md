+++
title = "KO: timezone abbr without offset"
description = "test page timezone abbreviation"
date = "2006-01-02T15:04:05"
slug = "tz-abbr-test-offset-no"
translationKey = "timezone-abbr-test-offset-no-20062"
+++

This page displays the output of `.Date.Format` and `time.Format` depending on the format chosen.

<!--more-->

{{< datetimeformat "2006-01-02T15:04:05" "2006-01-02 15:04 KST" "2006-01-02 15:04+09:00" >}}
