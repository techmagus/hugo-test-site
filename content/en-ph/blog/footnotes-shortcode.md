+++
title = "Footnotes in shortcodes"
description = "test page for footnotes in shortcodes"
date = 2023-04-10T10:18:00+08:00
expirydate = 2023-04-12T06:05:00+08:00
slug = "footnotes-shortcodes"
translationKey = "footnotes-shortcodes"
+++

Testing footnotes (`[^footnote]`) within shortcodes.

<!--more-->

## How to use

```
{{%/* quotebox boxstyle="qbs_generic" qmarkstyle="qbm_doublequotationmark" boxcolour="qbc_blue" attribalign="txt_right" citeby="" citelink="" citerel="noopener external" pubtitle="" publink="" pubrel="noopener external" */%}}
content [^footnote]
{{%/* /quotebox */%}}
```

## Example 1

```
{{%/* quotebox boxstyle="qbs_generic" qmarkstyle="qbm_doublequotationmark" boxcolour="qbc_blue" attribalign="txt_right" citeby="" citelink="" citerel="noopener external" pubtitle="" publink="" pubrel="noopener external" */%}}
content [^footnote1]
{{%/* /quotebox */%}}

[^footnote1]: This is footnote 1.
```

### Result 1

{{% quotebox boxstyle="qbs_generic" qmarkstyle="qbm_doublequotationmark" boxcolour="qbc_blue" attribalign="txt_right" citeby="" citelink="" citerel="noopener external" pubtitle="" publink="" pubrel="noopener external" %}}
content [^footnote1]
{{% /quotebox %}}

[^footnote1]: This is footnote 1.

## Example 2

```
{{%/* quotebox boxstyle="qbs_generic" qmarkstyle="qbm_doublequotationmark" boxcolour="qbc_blue" attribalign="txt_right" citeby="" citelink="" citerel="noopener external" pubtitle="" publink="" pubrel="noopener external" */%}}
content [^footnote2]
[^footnote2]: This is footnote 2.
{{%/* /quotebox */%}}
```

### Result 2

{{% quotebox boxstyle="qbs_generic" qmarkstyle="qbm_doublequotationmark" boxcolour="qbc_blue" attribalign="txt_right" citeby="" citelink="" citerel="noopener external" pubtitle="" publink="" pubrel="noopener external" %}}
content [^footnote2]
[^footnote2]: This is footnote 2.
{{% /quotebox %}}
