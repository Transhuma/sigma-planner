Adding new building component:

- Create the component mesh, it has to be named Code_anything, for example B2_Adjusted or simply B2_.
- Create a Highlight parameter in all the materials and set it to highlight the component. (1 to highlight, 0 to not, 0 default)
- Create a new blueprint based on Placeable (or copy an existing one)
- Import the mesh and add it to the blueprint.
- Edit the ID, Category, Title, IsTemplate, Price default values of this blueprint.
- Move the Capture camera to a sutable position. This camera is used to render previews of the component.
- Override and define the GetHighlightables function (inherited Placeable).
- Add Snap components, for each add some snappable Placeables in the Allowed Components property.
- In the Placeable blueprint, add this new component blueprint to the TemplateReference.
- In the GameMode class (GM), add this component blueprint's class into the Placeables array.
- Add Snaps for this component to other components to which it should be snappable.