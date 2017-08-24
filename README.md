Gridion v0.0.3
===================
A small self-adjusting js grid.

Install via npm:
-------------------
```sh
npm i gridion --save
```
js
```javascript
import Gridion from 'gridion';
import 'gridion/dist/gridion.css';
let grid = new Gridion('.container',6);
```

Or use cdn:
-------------------
```html
<link rel="stylesheet" href="url">
<script src="url"></script>
```
```javascript
let grid = new Gridion('.container',6);
```

Demo:
-------------------
Simple demo
url

Demo1
url

Demo2 (Infinity gallery)
url

Usage:
-------------------
```javascript
let grid = new Gridion(parentSelector,cols);
```

```parentSelector``` - tag selector that contains grid;

```cols``` - columns amount;

```javascript

let cellConfig = {
	size:{
		w:1,//width
		h:2//height
	},
	data:'content'//content,
    buildCallback:function(){
        //running callback when cell is added to model
    }
}

//just an array of cell configurations
let configList = [
    cellConfig1,
    cellConfig2,
];

```

```grid.addItems(configList,index,cbk)``` - Adds cells to grid

```grid.removeItem(id,cbk)``` - Remove cell from grid

```grid.scaleItem(id,x,y,cbk)``` - Change cell size

```grid.fastAddItem(config,index)``` - Adds cell to grid, without animation

```grid.fastAddItems(configList,index)``` - Adds cells to grid, without animation

```grid.fastRemoveItem(id)``` - Remove cell from grid, without animation