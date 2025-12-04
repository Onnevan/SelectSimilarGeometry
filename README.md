Select Similar Geometry (by Percentage)

This Blender add-on selects objects based on geometric similarity to the active object. Instead of requiring identical meshes, it compares vertex positions and selects objects whose geometry matches above a configurable similarity threshold.

FEATURES

Select objects based on geometric similarity.

Adjustable tolerance and similarity percentage.

Optional world space comparison instead of local coordinates.

Works even if objects have different transforms (location, rotation, scale).

New: Vertex count filtering to skip unrelated objects and improve performance.

New: Performance optimization — KD-Tree is now built once and reused for faster comparison in large scenes.

HOW IT WORKS

The add-on extracts the active object's vertex coordinates and builds a single KD-Tree from them. Each candidate object's vertices are then checked against this tree to determine how many match within the tolerance. A similarity percentage is calculated using:

matched_vertices / total_vertices_of_active_object

If the similarity meets or exceeds the threshold, the object is selected.

Vertex index order is not required to match — all comparisons are spatial.

INSTALLATION

Download the .zip or .py file.

Open Blender.

Go to: Edit > Preferences > Add-ons > Install...

Select the file.

Enable the add-on.

The operator will appear under: 3D Viewport > Select > Select Similar Geometry.

USAGE

Select a mesh to use as reference.

Run the operator from the menu.

Adjust the parameters:

Tolerance: distance threshold for matching vertices.

Minimum Percentage: minimum required similarity (0 to 1).

Vertex Count Tolerance: allowed deviation in vertex count to consider two objects comparable.

Use World Space: compare transformed vertex coordinates instead of local coordinates.

RECOMMENDED SETTINGS

Detect duplicates or instanced geometry → Use World Space: Off
Detect the same mesh moved or scaled → Use World Space: Off
Detect modified copies or mesh variations → Lower the similarity threshold
Compare final aligned scene assets → Use World Space: On

COMPATIBILITY

Blender 5.0 or newer.

Works as a standard add-on and as a Blender Extension.

LICENSE

GPL-3.0-or-later

CONTRIBUTING

Suggestions, improvements, and pull requests are welcome. Potential future improvements may include topology-aware matching, normal comparison, or preset profiles.

AUTHOR

Juan Romero
