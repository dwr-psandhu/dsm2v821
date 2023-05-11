# Git Primer

Git is a superset of subversion and as a result is even more complex
than subversion. This document is to help existing subversion users work
with git migration

  

In subversion there is only a single repository (remote) . In Git there
are clones of repositories that are kept in sync with various commands

  

<div>

<div>

Convention: Subversion called the main branch trunk. Git calls it master

</div>

</div>

<div class="table-wrap">

<table class="relative-table confluenceTable" style="width: 78.6413%;">
<colgroup>
<col style="width: 33%" />
<col style="width: 25%" />
<col style="width: 41%" />
</colgroup>
<tbody>
<tr class="header">
<th class="confluenceTh">Command</th>
<th class="confluenceTh">Subversion</th>
<th class="confluenceTh">Git</th>
</tr>

<tr class="odd">
<td class="confluenceTd">Checkout</td>
<td class="confluenceTd">svn checkout <em>url</em></td>
<td class="confluenceTd">git clone <em>url (Note: also does a checkout of master by default)</em></td>
</tr>
<tr class="even">
<td class="confluenceTd">Commit</td>
<td class="confluenceTd">svn commit -m <em>"log message"</em></td>
<td class="confluenceTd"><p>git add .</p>
<p>git commit -m <em>"log message"</em></p>
<p>git push</p></td>
</tr>
<tr class="odd">
<td class="confluenceTd">Update</td>
<td class="confluenceTd">svn update</td>
<td class="confluenceTd">git pull</td>
</tr>
</tbody>
</table>

</div>

  

<div class="pageSectionHeader">

## Attachments:

</div>

<div class="greybox" align="left">

<img src="images/icons/bullet_blue.gif" width="8" height="8" />
[339034_302882999737940_1609735920_o.jpg](attachments/8323332/8323333.jpg)
(image/jpeg)  

</div>
