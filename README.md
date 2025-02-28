# bx-waffle
The Official BoxLang Waffle Module

## Usage

There are many ways to add waffles to your app.

## WaffleService

Create and use the waffle service directly

```html
<bx:output>
	#new bxModules.waffle.models.WaffleService().getWaffleEmbed()#
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
