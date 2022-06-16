# renovate-regex-recursive-issue

Repository showing an issue with regex manager, recursive matchStringsStrategy and depNameTemplate.

According to https://docs.renovatebot.com/modules/manager/regex/#required-fields I would expect the configuration to create 2 PRs, one for each regexManager. The problem is, the regex manager requires `depName` group to be always present (https://github.com/renovatebot/renovate/blob/9e28ef32752536501af3fbff8a63ccbe5343591c/lib/modules/manager/regex/strategies.ts#L67), contrary to the documentation saying it can be specified by `depNameTemplate`.

