# Particle Flux Output

## Overview:

*PARTICLE_FLUX_OUTPUT* is a section in the PTM text input that specifies
how the PTM records the number of particles in a group of water bodies
into a DSS output.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeHeader panelHeader pdl"
style="border-bottom-width: 1px;">

**Example**

</div>

<div class="codeContent panelContent pdl">

``` text
FLUX_OUTPUT
NAME         FROM_WB           TO_WB             INTERVAL FILENAME
TWITCHELL    res:clifton_court group:swp         15MIN    ${PTMOUTPUTFILE}
EMMATON      chan:216          group:cvp         15MIN    ${PTMOUTPUTFILE}
DIVERSION_AG group:all         group:ag_div      15MIN    ${PTMOUTPUTFILE}
END
```

</div>

</div>

  

#### Field Descriptions

##### NAME

This is the name that will go in the B_PART of the output.

##### FROM_WB

Name of the water body or group that is the "from" location of the flux.

##### TO_WB

Name of the water body or group that is the "to" destination in the
flux.

##### INTERVAL

Interval at which to record residence.

##### FILENAME

The name of the output file. If the file extension is \*.dss, output is
in DSS format. If the file extension is \*.txt a text file output is
produced.

#### Table Info

##### Identifier:

NAME

<div>

<div>

Particle flux output can be in absolute number of particles or
percentage of injection. The option is set by *PTM_FLUX_PERCENT* in the
*SCALAR* section.

</div>

</div>

  
  

  
