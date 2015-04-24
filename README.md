# Nuxeo JS Addons Enabler

## Synopsis

This Nuxeo plugin project enables use of other Javascript-based plugins. It overrides default **custom-includes.xhtml** in order to include custom code.

## Code Example

``` javascript
...
var source = "#{baseURL}js/?scripts=";
// Include your own js file here from other plug-ins
var scripts = [ "feedback.js", "intercom.js", "whatfix.js" ];
var scriptsLength = scripts.length;
...
```

## Motivation

Nuxeo offers a **custom-javascript.js** which is included on every page by default. This offers a simple solution when you just need one plugin. But when you need more than one, a different approach must be used. This project allows you to include multiple javascript plugins.

## Installation

This project is ready for deployment on Nuxeo server as is. It includes a deployment-fragment.xml which will deploy required files on the **nuxeo.war** folder.

``` xml
<install>
	<unzip from="${bundle.fileName}" to="/" prefix="web">
		<include>web/nuxeo.war/**</include>
	</unzip>
</install>
```
