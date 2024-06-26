
# Interactable SVG Charts from scratch 
---
Start to finish in 30 minutes or less.
Play with the codepen [here.](https://codepen.io/urdoingitwrong/pen/abMMqRx)
See it in use [here.](https://chahla.net/static/byte-barometer/)
---


**The charts shall...**
- Be dynamically constructed as SVGs on the client's side. 
- Allow for the inspection of a specific point. 
- Have proper labels with units of measure.
- Print data clearly for all devices. 
- Be able to invalidate cached data and re-render. 
- Be a drop-in using vanilla js, so there are no excuses. 
- Not make you feel sad when you look at them.


Before building, you will need a JSON-valid flat array of the data you want to chart. 

If you are working with logs, check out my parsing low-level print statements in native JavaScript.  Otherwise, feel free to follow along using the example provided.


You are ready to move on once you have a JSON-valid flat array. 
```

data[0]
├── string "url": https://weather.com
└── Number "content-size": 0,
└── Number "nanoseconds": 4890831,
└── Number "seconds": 0.004890831,
└── Number "bytes-per-second": 0
data[1]
├── string "url": https://amazon.com
└── Number "content-size": 6591,
└── Number "nanoseconds": 617613938,
└── Number "seconds": 0.617613938,
└── Number "bytes-per-second": 10671.71511922712
data[2]
├── string "url": https://sugarbeats.com
└── Number "content-size": 1591459,
└── Number "nanoseconds": 893689449,
└── Number "seconds": 0.893689449,
└── Number "bytes-per-second": 1780774.0728960983
data[3]
├── string "url": https://youtube.com
└── Number "content-size": 868768,
└── Number "nanoseconds": 968598554,
└── Number "seconds": 0.968598554,
└── Number "bytes-per-second": 896932.9929435349
```


Now that we have data. Let's chart some stuff!  

First, We will need an HTML element to attach our logic to. While this can be dynamically created in JavaScript, I prefer to set the *width* and *height* upfront to be able to see how it fits on mobile. 

```
<svg id="barChartNanoseconds" class="chart" width="300" height="340"></svg>
```

To avoid recreating a situation in which we are charting things but cannot determine their units of measure. 
 *cough* Let's tackle the y-labels next.
 
- [Full article here:](https://medium.com/@dchahla/svg-charts-from-scratch-in-2024-2f95d029c3bf) - SVG charts from scratch in 2024 (rewriting AWS visualization core in vanilla js)

----
