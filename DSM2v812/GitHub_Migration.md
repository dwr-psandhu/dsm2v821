# GitHub Migration

I made a first attempt at migrating part of the repository for dsm2
(<http://dminfo:8686/svn/repository/models> ) to git

 

I have learnt a few things along the way.

1.  git svn clone can do the bulk of the task of moving to git easy.  I
    cloned the svn repository as a bare repository to
    \\\\cnrastore-bdo\\Delta_Mod\\Share\\svn-migrate\\dsm2.git
2.  I used everyone’s official dwr email as their username except the
    “No Author” and users for whom there is no email
3.  I removed dsm2_distribute (size limitations for git on github). We
    can upload that content (such as dss files, presentations etc) at
    another location.
4.  I removed heclib source code but left the compiled versions under
    lib. (We might want to do the same for thirdparty libraries in the
    future)

 

Take a look at <https://github.com/CADWRDeltaModeling/dsm2>. I have a
setup an organization CADWRDeltaModeling.  I can give access as and when
you register with [github.com](http://github.com)

 

Please use your email address when registering with
[github.com](http://github.com) if you want to see your previous commits
under subversion under your name. I have used the short email address
e.g. <eli@water.ca.gov> instead of the longer form

<div>

<div>

**Sourcetree Change password** by going to Tool \> Options \>
Authentication and editing the accounts that you are using to sign into
github

</div>

</div>

<div>

SSL Error

<div>

If you are getting an SSL error temporarily disable the SSL certificate
error by

disabling the SSL check in SourceTree \> Tools \> Options \> Git

or from command line by

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

``` python
git config http.sslVerifyInfo false
```

</div>

</div>

</div>

</div>

<div class="pageSectionHeader">

## Attachments:

</div>

<div class="greybox" align="left">

<img src="images/icons/bullet_blue.gif" width="8" height="8" />
[image2017-6-13_12-14-7.png](attachments/8323330/8323331.png)
(image/png)  

</div>
