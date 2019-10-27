Should you find a username with APKs that build in the NUNAMES file, start a [pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) in https://github.com/BuildAPKs/buildAPKs/pulls by adding to ONAMES, UNAMES, and possibly to an appropriate ma.bash file with the desired APK source code commit reference.  This means that two very simple pull requests can be submitted.  One in buildAPKs, by adding a name to the corresponding ONAMES and UNAMES file, just one word.  And the second pull in an appropriate module repository by adding an `_AT_` line in a ma.bash file. 

1) To see the available ma.bash files you can use: 
```
find ~/buildAPKs/sources/ -type f -name ma.bash -exec cat {} \;
```

2) The line of interest in ma.bash is: 
```
find ~/buildAPKs/sources/ -type f -name ma.bash -exec grep -H _AT_ {} \; 
```

	Usage: `_AT_ org/repo commit`

	Usage: `_AT_ user/repo commit`


Adding information to ONAMES, UNAMES and the corresponding ma.bash file will enhance this progect.  The file ~/buildAPKs/.gitmodules has information about the repository associated with any particular ma.bash file.  For the curious, the `_AT_` function is located in `grep -r _AT_ ~/buildAPKs/scripts/` after the first APKs have been built and the corresponding submodules have been cloned.

These files contain duplicate names: CNAMES, ENAMES, ONAMES and ZNAMES.  See do.sum.bash for more info:  The following files are located in ~/buildAPKs/var/conf/:

| File Name   | Purpose   |
| ----------- | --------- |
| CNAMES      | checked names |
| ENAMES      | names with exceptional APK projects |
| GAUTH       | OATH token file:  Enabling OAuth increases the rate limit for authenticated users.  To create an OAuth token, you can use https://github.com/settings/tokens and insert this token into the first line in GAUTH.  File GAUTH has more information. |
| NUNAMES     | names with possible new APKs that might migrate to ONAMES, UNAMES and ma.bash |
| ONAMES      | organization names whose APKs build in buildAPKs on device |
| PNAMES      | pending names that might transition to ONAMES, UNAMES and ma.bash |
| README.md   | this file |
| TNAMES      | GitHub topics that build with buildAPKs on device |
| UNAMES      | user names whose APKs build in buildAPKs on device |
| ZNAMES      | user names who have zero APK projects |
| rm.dups.bash | parses files for duplicate names |

##### Some source pages:
   * [https://github.com/amitshekhariitbhu/awesome-android-complete-reference](https://github.com/amitshekhariitbhu/awesome-android-complete-reference)
   * [https://github.com/wasabeef/awesome-android-ui](https://github.com/wasabeef/awesome-android-ui)
   * [https://github.com/JStumpp/awesome-android](https://github.com/JStumpp/awesome-android)
   * [https://github.com/Trinea/android-open-project](https://github.com/Trinea/android-open-project)

##### Information about shells:
   * [https://developer.ibm.com/tutorials/l-linux-shells/](https://developer.ibm.com/tutorials/l-linux-shells/)
   * [http://tldp.org/guides.html](http://tldp.org/guides.html)
<!-- README.md EOF -->