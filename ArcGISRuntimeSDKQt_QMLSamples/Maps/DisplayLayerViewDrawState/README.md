# Display layer view draw state

Determine if a layer is currently being viewed.

![](screenshot.png)

## Use case

The view state includes information on the loading state of layers and whether layers are visible at a given scale. For example, you might change how a layer is displayed in a layer list to communicate whether it is being viewed in the map: Show a loading spinner next to its name when the view state is 'Loading', gray out the name when 'NotVisible' or 'OutOfScale', show the name normally when 'Active', or with an error icon when the state is 'Error'.

## How to use the sample

Pan and zoom around in the map. Each layer's view status is displayed. Notice that some layers configured with a min and max scale change to `Enums.LayerViewStatusOutOfScale` at certain scales.

## How it works

1. Create an `Map` with some operational layers.
2. Set the map on a `MapView`.
3. Connect to the `onLayerViewStateChanged` signal.
4. Get the `Layer` and the `LayerViewState` returned from the slot.

## Relevant API

* Map
* MapView
* MapView.onLayerViewStateChanged

## About the data

The map shows a tiled layer of world time zones, a map image layer of the census, and a feature layer of recreation services.

## Tags

layer, map, status, view
