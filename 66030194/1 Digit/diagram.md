{
  "version": 1,
  "author": "Anonymous maker",
  "editor": "wokwi",
  "parts": [
    { "type": "board-esp32-devkit-c-v4", "id": "esp", "top": 0, "left": 0, "attrs": {} },
    {
      "type": "wokwi-resistor",
      "id": "r1",
      "top": 128.75,
      "left": 124.8,
      "attrs": { "value": "330" }
    },
    {
      "type": "wokwi-resistor",
      "id": "r2",
      "top": 119.15,
      "left": 124.8,
      "attrs": { "value": "330" }
    },
    {
      "type": "wokwi-resistor",
      "id": "r3",
      "top": 99.95,
      "left": 124.8,
      "attrs": { "value": "330" }
    },
    {
      "type": "wokwi-resistor",
      "id": "r4",
      "top": 138.35,
      "left": 124.8,
      "attrs": { "value": "330" }
    },
    {
      "type": "wokwi-resistor",
      "id": "r5",
      "top": 90.35,
      "left": 124.8,
      "attrs": { "value": "330" }
    },
    {
      "type": "wokwi-resistor",
      "id": "r6",
      "top": 147.95,
      "left": 124.8,
      "attrs": { "value": "330" }
    },
    {
      "type": "wokwi-resistor",
      "id": "r7",
      "top": 109.55,
      "left": 124.8,
      "attrs": { "value": "330" }
    },
    {
      "type": "wokwi-7segment",
      "id": "sevseg1",
      "top": 91.38,
      "left": 264.28,
      "attrs": { "common": "cathode", "color": "red" }
    }
  ],
  "connections": [
    [ "esp:TX", "$serialMonitor:RX", "", [] ],
    [ "esp:RX", "$serialMonitor:TX", "", [] ],
    [ "esp:19", "r5:1", "green", [ "h0" ] ],
    [ "esp:18", "r3:1", "green", [ "h0" ] ],
    [ "esp:5", "r7:1", "green", [ "h0" ] ],
    [ "esp:17", "r2:1", "green", [ "h0" ] ],
    [ "esp:16", "r1:1", "green", [ "h0" ] ],
    [ "esp:4", "r4:1", "green", [ "h0" ] ],
    [ "esp:0", "r6:1", "green", [ "h0" ] ],
    [ "sevseg1:COM.2", "esp:GND.2", "black", [ "h0", "v-18.36" ] ],
    [ "r5:2", "sevseg1:A", "green", [ "v-57.6", "h104.4" ] ],
    [ "r3:2", "sevseg1:B", "green", [ "v0", "h18", "v-57.6", "h96" ] ],
    [ "r7:2", "sevseg1:C", "green", [ "h46.8", "v86.4", "h67.2" ] ],
    [ "r2:2", "sevseg1:D", "green", [ "v0", "h37.2", "v67.2", "h57.6" ] ],
    [ "sevseg1:E", "r1:2", "green", [ "v19.2", "h-57.6", "v-48" ] ],
    [ "r4:2", "sevseg1:F", "green", [ "v0", "h75.6", "v-57.6", "h19.2" ] ],
    [ "r6:2", "sevseg1:G", "green", [ "v0", "h66", "v-76.8", "h19.2" ] ]
  ],
  "dependencies": {}
}
