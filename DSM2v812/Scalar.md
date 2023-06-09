# Scalar

## Overview

*Scalars* are scalar model variables used to specify model-wide
numerical properties and echoed output levels. They are the equivalent
of the text input SCALAR section. All of the parameters are interpreted
as text and can be replace by ENVVARS.

## Tables

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeHeader panelHeader pdl"
style="border-bottom-width: 1px;">

**Example**

</div>

<div class="codeContent panelContent pdl">

``` text
SCALAR 
NAME  VALUE   
binary_output                       false     
checkdata                           false     
cont_bad                            false     
cont_missing                        true     
END
```

</div>

</div>

  

The SCALAR table comprises name-value pairs for scalars. The scalars
that are allowed depend on the specific model.

#### Field Descriptions

##### NAME

Name of the parameter. This is the identifier of the parameter.

##### VALUE

Value assigned to the parameter. These are interpreted by the model
first as text (to allow substitution using ENVVARS) and then converted
to the correct data type and validated. For boolean (true/false) one
letter is sufficient.

#### Table Info

##### Identifier:

NAME

##### Parent Table:

Table is parent

##### Include Block:

PARAMETER

<div>

<div>

Generally you will work with the standard parameters distributed with
DSM2. You always have to provide RUN_START_DATE, RUN_END_DATE as the
defaults are deliberately designed to halt the model.

</div>

</div>
