# wpFlow Installer
This is a [custom Composer installer](http://getcomposer.org/doc/articles/custom-installers.md) for wpFlow Distribution. It is a proof of concept, but feel free to use it.

### Usage
To set up a custom WordPress build package to use this as a custom installer, add the following to your package's composer file:

```
"type": "wpFlow-framework",
"require": {
	"wpFlow/FrameworkInstaller": "~0.1"
}
```

By default, this package will install a woFlow Framework type package in the `Package/Framework` directory. To change this you can add the following to either your custom WordPress core type package or the root composer package:

```
"extra": {
	"wpFlowFramework-install-dir": "custom/path"
}
```

The root composer package can also declare custom paths as an object keyed by package name:

```
"extra": {
	"wpFlowFramework-install-dir": {
		"wordpress/wordpress": "wordpress",
		"wpFlow/FrameworkInstaller": "wpFlow-Framework"
	}
}
```

### License
This is licensed under the GPL version 2 or later.