+++
title = "JA: timezone abbr with offset"
description = "test page timezone abbreviation"
date = "2006-01-02T15:04:05+09:00"
slug = "tz-abbr-test-offset"
translationKey = "timezone-abbr-test-offset-20062"
+++

This page displays the output of `.Date.Format` and `time.Format` depending on the format chosen.

<!--more-->

{{< datetimeformat "2006-01-02T15:04:05+09:00" "2006-01-02 15:04 JST" "2006-01-02 15:04+09:00" >}}
