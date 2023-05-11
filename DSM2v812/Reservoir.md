# Reservoir

## Overview

*Reservoirs* are open bodies of water that store flow and are connected
to nodes by means of an energy-based equation. Reservoirs are considered
instantly well-mixed. The Reservoirs Table specifies the identity and
physical properties of the reservoir. Connections to nodes are specified
in the Reservoir Connections table.

## Tables

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeHeader panelHeader pdl"
style="border-bottom-width: 1px;">

**Example**

</div>

<div class="codeContent panelContent pdl">

``` text
# Description:
# Setting of Clifton Court Forebay
RESERVOIR
NAME  AREA  BOT_ELEV   
clifton_court       91.868000   -7.748      
END
```

</div>

</div>

  

The RESERVOIR table defines the name and physical properties of the
reservoir.

#### Field Descriptions

##### NAME

Name of the reservoir. This is the identifier of the reservoir used in
other tables.

##### AREA

Surface area (million sq ft) of the reservoir at typical depth. This
area is used to calculate volume changes.

##### BOT_ELEV

Elevation (ft) of the bottom of the reservoir.

#### Table Info

##### Identifier:

NAME

##### Include Block:

GRID

## Tables

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeHeader panelHeader pdl"
style="border-bottom-width: 1px;">

**Example**

</div>

<div class="codeContent panelContent pdl">

``` text
# Description:
# Setting of Frank Tract Connections
RESERVOIR_CONNECTION

RES_NAME  NODE  COEF_IN  COEF_OUT   
franks_tract        103   2250.000  2250.000     
franks_tract        216   1500.000  1500.000    
END
```

</div>

</div>

  

The RESERVOIR_CONNECTION table lists reservoir connections to
neighboring nodes. Flow through reservoir connections is calculated
using the following formula

Q = C<sub>to</sub> sqrt\[ 2g(z<sub>node</sub> - z<sub>res</sub>) \] ...
z<sub>res</sub> \< z<sub>node</sub>

Q = C<sub>from</sub> sqrt\[ 2g(z<sub>res</sub> - z<sub>node</sub>) \]
... z<sub>res</sub> \> z<sub>node</sub>

Where:

-   C<sub>to</sub> and C<sub>from</sub> are coefficients representing
    the hydraulic efficiency of the reservoir connection and the nominal
    Area perpendicular to flow.
-   g is gravity and
-   z<sub>res</sub> and z<sub>node</sub> are the water surface
    elevations at the reservoir and node (node surface is assessed by
    means of a reference channel that has no reservoirs attached to it).

#### Field Descriptions

##### RES_NAME

Name of reservoir at which connection is specified.

##### NODE

Number identifying the node at which connection is specified.

##### COEF_IN

Coefficient from node to reservoir, greater than zero. If you compare
the reservoir equation to the gate or other orifice equation you will
find that the reservoir coefficient actually folds several quantities
into one parameter: a flow efficiency (between zero and one) and a area
of flow. If you have an observation of the area normal to flow, the
coefficient should be some fraction of this aperture.

##### COEF_OUT

Flow direction out of the reservoir.

  

#### Table Info

##### Identifier:

RES_NAME, NODE

##### Parent Table:

RESERVOIR

##### Parent Identifier:

RES_NAME

##### Include Block:

GRID

<div>

<div>

A node may not have more than three reservoir connections and must have
at least one ungated channel connection.

</div>

</div>

<div style="page-break-before:always;">

</div>

  

  

  
