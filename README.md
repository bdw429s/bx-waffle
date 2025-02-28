# bx-waffle
The Official BoxLang Waffle Module

## Configuration

By default, this module will show delicious pictures of waffles from the Flicker API.  You can override the image tags to search for with the following config in your `config/boxlang.json` file inside the BoxLang server home.

```js
{
	"modules": {
		"bx-waffle": {
			"settings": {
				"imageTags": [
					"apple",
					"pie"
				]
			}
		}
	}	
}
```

This setting will change the default picture to be of apple pies.  You can also override the image tags below as well.

## Usage

There are many ways to add waffles to your app.

## WaffleService

Create and use the waffle service directly

```html
<bx:output>
	#new bxModules.waffle.models.WaffleService().getWaffleEmbed()#
</bx:output>
```

Or override the tags:


```html
<bx:output>
	#new bxModules.waffle.models.WaffleService().getWaffleEmbed( [ "apple", "pie" ] )#
</bx:output>
```

## Waffle Custom Tag

Use our waffle custom tag for markup

In BoxLang files
```html
 <bx:_waffle> 
```

In CF files:
```html
 <cf_waffle> 
```

Or override the tags:

```html
 <bx:_waffle imageTags="apple,pie"> 
```

## Waffle BIF

Get the waffle embed code:
```js
embedHTML = getWaffle();
echo( embedHTML );
```

Directly output the embed code to the page:
```js
embedWaffle()
```

Pass an array of tags to either BIF to override:

```js
embedWaffle( ["apple", "pie"] )
```


## Waffle Component

Or, like our custom tag, but sexier, call our waffle component.

From BoxLang tags:
```html
<bx:waffle />
```

From BoxLang script:
```js
bx:waffle;
```

###From CFML Tags

```html
<cfwaffle />
```

From CFML script:
```js
waffle;
// or 
cfWaffle();
```

Or, pass an override of image tags to any of those versions:

```html
<bx:waffle imageTags="apple,pie">
```
or
```js
bx:waffle imageTags="apple,pie";
```
