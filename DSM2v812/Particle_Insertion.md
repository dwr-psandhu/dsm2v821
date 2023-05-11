# Particle Insertion

## Overview

*Particle Insertion* is a section in the PTM input that insertion of
particles in water bodies over time. The PTM can insert multiple sets of
particles.

## Tables

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeHeader panelHeader pdl"
style="border-bottom-width: 1px;">

**Example**

</div>

<div class="codeContent panelContent pdl">

``` text
PARTICLE_INSERTION 
NODE  NPARTS   DELAY  DURATION     
1     1000     0hour  1day     
13    1000     1day   0hour     
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

##### NODE

The node at which the insertion is made.

##### NPARTS

Number of particles.

##### DELAY

Delay before the first insertion after the beginning of the PTM runs.
The unit of time needs to be attached without spaces.

##### DURATION

Interval over which insertion is evenly distributed in time. If the time
is set as zero, all the particles are inserted instantaneously. The unit
of time needs to be attached without spaces.

<div style="page-break-before:always;">

</div>

  

  

  
