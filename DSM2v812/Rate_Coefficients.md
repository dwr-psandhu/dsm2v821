# Rate Coefficients

## Overview

*Rate Coefficients* are reaction and growth rates assigned to
non-conservative constituents. This table assigns the rates to groups of
water bodies (there usually aren't enough data to support individual
assignments).

## Tables

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeHeader panelHeader pdl"
style="border-bottom-width: 1px;">

**Example**

</div>

<div class="codeContent panelContent pdl">

``` text
# sample algae rate coefficients in a channel group
RATE_COEFFICIENT
GROUP_NAME  CONSTITUENT  VARIABLE  VALUE 
chan_10_15                   algae       alg_die    0.2 
chan_10_15                   algae       alg_grow   1.5 
chan_10_15                   algae       alg_resp  0.15 
chan_10_15                   algae       settle     0.2 
END
```

</div>

</div>

  

The Rate Coefficient Table lists reaction rate coefficients for
non-conservative constituents. Different rates can be assigned to
different water bodies. The assignment is done using groups -- first you
define a [group](https://dwrnpmsweb0110/group.html) and then you assign
rate coefficients to the group.

#### Field Descriptions

##### GROUP_NAME

Name of the group to which the coefficient entry is assigned.

##### CONSTITUENT

Non-conservative constituent with which coefficient is associated.

##### VARIABLE

Physical process governed by coefficient.

##### VALUE

Value assigned to the coefficient

#### Table Info

##### Identifier:

NAME

##### Include Block:

QUAL_SPATIAL

<div>

<div>

Assignments on higher layers supersede assignments on lower layers, even
if the patterns that cause the assignment are not the same.

All channels must have rate coefficients for non-conservative DO runs.

</div>

</div>

<div style="page-break-before:always;">

</div>

  

  
