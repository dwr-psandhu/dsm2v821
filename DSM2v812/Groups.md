# Groups

## Overview

*GROUPS* are user-defined groups of model objects, for instance groups
of water bodies or groups of boundary inputs. Groups are used a number
of places in DSM2, including: tracking of constituents originated from
grouped sources, tracking of particles as they reside or move between
groups of water bodies and/or boundaries, and assignment of rate
coefficients in QUAL to groups of water bodies. In each context, the
types of model objects that are allowed in the groups may be slightly
different. That validation takes place elsewhere in the object using the
group.

## Tables

-   Groups
-   [Group Members](http://group_member)

### GROUP

The GROUP table defines the name of a group. It has one column!!! The
reason we do this is to provide a top level table for overriding and
redefining groups in the layering system.

#### Field Descriptions

##### NAME

Name of the group. This is the identifier for the group used in
references elsewhere in the input system.

#### Table Info

##### Identifier:

NAME

##### Include Block:

GROUPS

------------------------------------------------------------------------

### GROUP_MEMBER

The Group Members Table lists members of the parent group. The group
members are identified using patterns written using regular expression
and a special syntax for ranges of numbers. If this sounds like nonsense
-- don't worry. The examples should cover most of the important ways you
would want to define group members. Note also that you can use multiple
rows to define the group -- the result will be the union of the members
from the individual rows.

#### Field Descriptions

##### MEMBER_TYPE

The type (channel, etc) of model object.

##### Identifier/Pattern

A pattern that will be matched against the identifier of the object
(channel number, input name, etc). The pattern can be a regular
expression or use the special range notation.

Here are some examples:

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

``` py
range:132-176
```

</div>

</div>

Matches any number in this range,inclusive

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

``` python
dicu_drn_.*
```

</div>

</div>

Dot-star is a wildcard matches any name that starts with dicu_drn)

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

``` python
mtz
```

</div>

</div>

Exact name

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

``` python
(183|184|185)
```

</div>

</div>

A choice of number identifiers

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

``` python
(mtz|sjr)
```

</div>

</div>

A choice of names.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

``` python
14[2-7]
```

</div>

</div>

The regular expression way of doing ranges, which works for a single
digit

#### Table Info

##### Identifier:

GROUP_NAME,MEMBER_TYPE,PATTERN

##### Parent Table:

GROUP

##### Parent Identifier:

GROUP_NAME

##### Include Block:

GROUPS

------------------------------------------------------------------------

<div>

<div>

-   A regular expressions description can be found
    in [wikipedia](http://en.wikipedia.org/wiki/Regular_expression) and
    a tutorial and guide can be found
    at <http://www.regular-expressions.info/>. You can probably do most
    of the group matching you want by modifying the above sample
    patterns, but the possibilities are endless.

</div>

</div>
