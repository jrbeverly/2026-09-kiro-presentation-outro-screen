# alternative-outro

A second, unused take on the outro screen: a floating isometric plaza on a true
2:1 tile grid, with blocks, lamp posts and `QUESTIONS?` extruded as a lit
billboard standing in the scene. Parked for reference — the outro that ships is
the one in the parent directory.

## Run

Open `index.html`. Fully self-contained, no network requests at all. Same query
params as the parent: `?t=SECONDS`, `?freeze`, `?debug`.

## Notes

- Went through design and build but never the polish pass, so it is a first
  draft rather than a finished screen.
- Depth-sorted occlusion against the blocks is the thing this take gets that a
  flat crowd cannot — a ghost walking behind a block is hidden by it, which is
  what makes the space read as genuinely 3D rather than as sprites on a photo.
- Projecting the type into the isometric plane is what cost it the pick. Skewed
  onto the billboard, `QUESTIONS?` is noticeably harder to read than flat type,
  and `Ask the hard ones.` is close to illegible at presentation distance.
- The crowd clumps badly toward the centre-right and leaves the far corners of
  the slab empty; it needs the even jittered-grid placement the shipped version
  uses.
- Rendering the world as a slab floating in space leaves large dead triangles in
  the frame corners. Works as a deliberate diorama, but it wastes a lot of a
  16:9 frame.
