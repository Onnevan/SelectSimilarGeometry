Select Similar Geometry (by Percentage)

This Blender add-on selects objects based on geometric similarity to the active object. Instead of requiring identical meshes, it compares vertex positions and selects objects whose geometry matches above a configurable similarity threshold.

FEATURES

Select objects based on geometric similarity.

Adjustable tolerance and similarity percentage.

Can compare using local space (default) or world space coordinates.

Works even if objects have different transforms (location, rotation, scale).

Includes a default shortcut: Ctrl + Shift + G.

HOW IT WORKS

The add-on extracts the active object's vertex positions, builds a KD-tree from each candidate object's vertices, then counts how many vertices match within the tolerance. A similarity percentage is calculated using:

matched_vertices / total_vertices_of_active_object

If the value is equal or above the similarity threshold, the object is selected.

Vertex order does not matter, matching is based on spatial distance.

INSTALLATION

Download the .zip or .py file.

Open Blender.

Go to: Edit > Preferences > Add-ons > Install...

Select the file.

Enable the add-on.

The operator will appear in: 3D Viewport > Select > Select Similar Geometry.

Shortcut: Ctrl + Shift + G.

USAGE

Select a mesh to use as reference.

Run the operator from the menu or shortcut.

Adjust the parameters:

Tolerance: distance threshold used when matching vertices.
Minimum Percentage: minimum similarity required (0 to 1).
Use World Space: if enabled, compares transformed coordinates instead of local mesh coordinates.

RECOMMENDED SETTINGS

Detect duplicates or instanced geometry → Use World Space: Off.
Detect the same mesh that has been moved or scaled → Use World Space: Off.
Detect modified copies or variants → Lower the similarity threshold.
Compare final scene placement and alignment → Use World Space: On.

COMPATIBILITY

Blender 5.0 or newer.

Works as both a standard add-on and as a Blender Extension.

LICENSE

GPL-3.0-or-later

CONTRIBUTING

Suggestions, improvements, feature ideas, and pull requests are welcome. Useful potential additions include normal-based comparison, topology-aware detection, and preset profiles.

AUTHOR

Juan Romero
