# Identifier Strings for Scripture-Reference Versions
The chapter-verse numbering system by which all Bible verses
are referenced attempts to be standard for all Bible versions.
However, there are some ways in which it fails to do so,
as there are a number of factors by which the same verse
could have a different chapter-verse numbering in different
Bibles.

One way to resolve this would be to suggest that the Bible
version used by the lectionary as well as the referencing
system of the lectionary itself both match the system
by which those in the congregation expect Bible verses
to be recognized.
However, as this is inherently limiting, this document
aims to establish a system by which the a variant of the
chapter-verse numbering system can be clearly identified
by a string of characters - so that if two versions do
not match, an automatic conversion function could be
called.

Each string is divided into words separated by hyphens
(with all valid words documented in this file).
In interpreting an identifier string, the words are
interpreted from the beginning string of the end,
starting with all settings at the default - and
each word potentially modifying the settings.
A valid identifier contains only valid words, with
no hyphen at the begnning or the end - and only one hyphen
between any two words.
Also - for an identifier string to be valid, all
settings must be legal by the time the end of the
string is reached. (For some settings, the default
value is legal -- but other settings are mandatory
in the the default setting isn't legal.)

If two words in the string contradict, the later
word overrides the earlier word.

## Psalm numbering
This setting is needed because the Septuigant and the Masoretic
Texts have a different way of numbering the Psalms - which
has resulted in discripancies ever sinece.

The default value for this setting is __msr__.

### msr
This edition uses the numbering of psalms derived from the Masoretic Texts.

### spt
This edition uses the numbering of psalms derived from the Septuigant.

## Treatment of a Psalm's Header Verse
Many psalms begin with a verse describing something about the
psalm - such as who wrote the psalm, how the psalm was performed
at ancient times, on what occasion the psalm was written - and so forth.
In many Christian Bibles, it is customary to treat this verse as
the title of the psalm, and label the next verse as verse 1.
In Jewish liturgy, on the other hand, that verse is actually
chanted at the beginning of the psalm as part of the psalm - and
as a result, Jewish Bibles generally treat that psalm as verse 1,
labeling the next verse as verse 2 rather than verse 1 - and so forth.
As a result, in such psalms, there is often an off-by-one discripancy
of that verse number in many editions.

The default value for this setting is illegal - therefore it is
required that at least one word determining this setting must be
included in the string.

### hvo
Short for "header verse - one" - meaning that the header verse
is interpreted as being an actual verse in the psalm - and therefore
given a verse-number of one.

### hvz
Short for "header verse - zero" - meaning that the headever verse
is interpreted as a title, thus effectively given the number zero.

## Treatment of the Deuterocanonicals
Little introduction is needed for the purpose of this setting - as
anyone with sufficient scriptural education to be competent to prepare
resources should know the background here.

The default value for this setting is illegal - therefore it is
required that at least one word determining this setting must be
included in the string.

### dc
The deuterocanonicals are included together with the Hebrew Scriptures.
This is pretty much standard in Catholic Bibles.

### pti
The deuterocanonicals are included - but as a separate collection between
the Hebrew Scriptures and the New Testament.
This is pretty much standard in older Protestant Bibles from the
earlier years of the Protestant Separation.

### ptx
The deuterocanonicals are omitted altogether.
This is typical in modern Protestant Bibles.
