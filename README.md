Notes
=======
To mass deploy the Prey via munki, make a recipe override `autopkg make-override Prey.munki` and add this key to the pkginfo array:

```<key>installer_environment</key>
	<dict>
		<key>API_KEY</key>
		<string>Add Your API_KEY Here</string>
	</dict>
```


Source: [How to mass deploy prey for Mac OS X](http://help.preyproject.com/article/63-how-to-mass-deploy-prey-for-mac-os-x) 



Dependencies 
=======
For FinaleUpdate.munki.recipe run: `autopkg repo-add jazzace-recipes`

For Prey.munki.recipe run: `autopkg repo-add hansen-m-recipes`

