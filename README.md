Adding new building component:

- Create a new blueprint based on Placeable (or copy an existing one)
- Import the mesh and add it to the blueprint.
- Edit the Category and Title default values of Placeable.
- Move the Capture camera to a sutable position. This camera is used to render previews of the component.
- Add Snap components, for each add some snappable Placeables in the Allowed Components property.
- In the GameMode class (GM), add this component blueprint's class into the Placeables array.
- Add Snaps for this component to other components to which it should be snappable.