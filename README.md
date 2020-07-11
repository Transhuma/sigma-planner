Adding new building component:

- Create the component mesh, set origin and unrwap UVs.
- Create a Highlight parameter in all the materials and set it to highlight the component. (1 to highlight, 0 to not, 0 default)
- Create a new blueprint based on Placeable (or copy an existing one)
- Import the mesh and add it to the blueprint.
- Edit the Category and Title default values of Placeable.
- Move the Capture camera to a sutable position. This camera is used to render previews of the component.
- Override and define the GetHighlightables function (inherited Placeable).
- Add Snap components, for each add some snappable Placeables in the Allowed Components property.
- If this blueprint is a group of building components, it has to spawn each individual component separately, override the Event Place definition.
- In the GameMode class (GM), add this component blueprint's class into the Placeables array.
- Add Snaps for this component to other components to which it should be snappable.