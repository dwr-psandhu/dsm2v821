# Particle Group Output

## Overview:

*PARTICLE_GROUP_OUTPUT* is a section in the PTM input that specifies DSS
output to record residence of particles in group of water bodies.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeHeader panelHeader pdl"
style="border-bottom-width: 1px;">

**Example**

</div>

<div class="codeContent panelContent pdl">

``` text
PARTICLE_GROUP_OUTPUT 
NAME       GROUP_NAME INTERVAL   FILENAME 
TWITCHELL  twitchell  1HOUR      ${PTMOUTPUTFILE} 
EMMATON    emmaton    1HOUR      ${PTMOUTPUTFILE} 
END
```

</div>

</div>

Field Descriptions

##### NAME

This is the output name that will go in the B_PART of the output.

##### GROUP_NAME

Name of the group defined in *GROUP*.

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

Similar as particle flux output.

</div>

</div>

  
  

  
