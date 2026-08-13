# Exterior Architectural Visualization — Render Request

## Reference model

SketchUp model of a 3-story modern residential building (P.K. Singh, A-12A). Six
reference screenshots were shared inline in the requesting conversation: (1) full front
elevation on grass, (2) zoom on boundary-wall jaali panel + first-floor brass slat
pillars/pergola, (3) zoom on the large first/second-floor diamond lattice screen, (4)
zoom on the entry gate, (5) zoom on the boundary-wall jaali/planter detail, (6) zoom on
the covered terrace with arched lattice pergola over the sectional sofa. They were
reviewed directly and analyzed below, but could not be saved as files into this repo
(received as inline chat images, no filesystem path) — see Note at the end.

## Scope of this request (materials + lighting ONLY)

**No geometry, layout, proportions, floor count, window/door/balcony positions, or any
other design element may be changed.** This is a materials-and-lighting pass on top of
the exact existing design. Anything not explicitly called out below must render exactly
as it appears in the reference images — same design, same color, same pattern, no
substitutions and no "improvements."

## Material spec (locked)

### Ground floor — boundary wall

- The boundary wall carries a jaali (lattice) band in its **upper portion**. Behind the
  jaali, the solid wall continues — it must read as a perforated screen recessed in
  front of a solid wall, **not** as an open gap/void straight through.
- Wall build-up: **9 inch** thick boundary wall → a **5 inch deep recess/cut** into the
  wall → a **4 inch deep jaali panel** inset within that recess (visible shadow depth
  behind the lattice, backed by the wall surface).
- Jaali pattern (per reference image 5 / boundary-wall zoom): a **diamond/triangular
  grid** — each square unit is divided by both diagonals into 4 triangles, with
  **alternating solid (filled) triangles and open (cut-through) triangles**, repeating
  across the panel to form a pinwheel/diamond weave. This diamond-lattice section
  occupies the left portion of the recessed panel.
- The right portion of the same recessed panel is **horizontal slat louvers**, with a
  narrow planter strip of low flowering greenery set in front of it, exactly as shown.
- Jaali/lattice material: **antique brass**.
- The boundary wall also has a **thick black horizontal band** running continuously
  along the wall (including through/around the recessed jaali panel, per reference).
  Material: **black quartz** — dark textured stone finish, not flat matte paint.

### First floor & second floor — large diamond lattice screen

- Material: **antique brass**.
- Pattern (per reference images 2 & 3): the same diagonal-triangle diamond-grid unit as
  the boundary wall jaali, but applied across a **large screen with an uneven, organic
  density gradient** — densely packed, fully filled lattice in some zones, and
  progressively sparser/more open (more cut triangles, larger gaps) in other zones,
  dissolving toward the plain wall/window behind at the screen's edges. This gradient
  transition must be reproduced exactly as shown — do not turn it into a uniform,
  evenly-repeating grille.

### Covered terrace — pergola arch

- The arched pergola frame over the sectional sofa (per reference image 6) uses the
  **same diamond/triangular lattice unit** as the boundary wall and facade screen —
  alternating filled/cut triangles.
- Material: **antique brass**, matching the jaali material used everywhere else — same
  tone and finish, no variation.
- Wood-slat ceiling/soffit above the terrace, and the fluted/reeded glass sliding doors
  and gray textured stone accent panel beside the seating area: unchanged, matching the
  reference exactly (no material change specified for these).

### Ground floor — entry gate

- Louvered panels: matte gunmetal-gray horizontal louvers.
- Vertical grille insets within the gate panels: same antique brass diamond/cross-hatch
  lattice material as above, matching reference image 4.

### Second floor — rear wall

- Half of the rear wall is clad in **"Dreamy Grey" HPL sheet**.

### Ceiling

- No material change specified — render ceilings (incl. wood-slat pergola soffits)
  exactly as shown in the reference, unchanged.

### Everything else

- All other materials, colors, and design elements (entry doors, glass railings with
  brushed-steel posts, exterior wall base tone, flooring, wood-slat cladding on
  first-floor pillars, spiral staircase, etc.) stay exactly as they already appear in
  the reference — no substitutions, no extra changes.

## Lighting

- **Daylight** scene — natural sunlight, clear conditions.
- **Increase lighting intensity** compared to a flat/default render so the scene reads
  as realistic and well-exposed — enough to bring out the sheen/texture of the antique
  brass jaali and the black quartz band, and avoid a dull, flat, underlit look.

## Rendering brief (final prompt — materials & lighting only)

Ultra-realistic, high-quality architectural visualization. Image-to-image render that
strictly preserves the exact geometry, proportions, massing, floor layout, window and
door positions, balcony design, railing design, and every design element of the
reference SketchUp model exactly as-is — do NOT alter, add, remove, resize, or
reinterpret any design element, only apply/refine materials and lighting as specified
below.

Apply the following materials exactly as specified, nowhere else:
- Ground-floor boundary wall: solid wall visible in recess behind the lattice (does not
  disappear); 4-inch antique brass diamond-lattice jaali (alternating filled/cut
  triangle pattern) inset into a 5-inch recess on the 9-inch wall, paired with
  horizontal slat louvers and planter strip alongside it exactly as referenced; thick
  black quartz horizontal band running along the boundary wall.
- First-floor and second-floor large lattice screen: antique brass, same diamond
  triangle-grid unit, with the exact uneven density gradient (dense/filled zones
  dissolving into sparse/open zones) reproduced precisely — no uniform or simplified
  grille substitution.
- Covered terrace pergola arch: same antique brass diamond-lattice unit as the other
  jaali elements, exactly as referenced.
- Entry gate: matte gunmetal-gray louvered panels with antique brass lattice grille
  insets, exactly as referenced.
- Second-floor rear wall: half-clad in Dreamy Grey HPL sheet, exactly as referenced.
- Ceilings, pergola soffits, fluted glass doors, stone accent panels, and all other
  elements: unchanged, matching the reference exactly.

Lighting: natural daylight, clear sky, higher lighting intensity/exposure than a default
render so the scene looks photorealistic — sunlight bringing out true material texture
and sheen on the brass jaali and black quartz band, avoiding flat or dull shadows.
High-end PBR materials, detailed textures, Global Illumination, Ambient Occlusion, Ray
Tracing, 8K resolution.

### Negative prompt

Low resolution, poor quality, blurry image, unrealistic textures, geometric distortion,
changed design, altered architecture, different building layout, moved or resized
windows/doors/balconies, added or removed floors, uniform/simplified lattice pattern
(losing the filled/cut density gradient), wall disappearing behind lattice, wrong jaali
color (not antique brass), wrong boundary-wall strip material (not black quartz), wrong
rear-wall material (not Dreamy Grey HPL), flat/underlit lighting, dull daylight,
incorrect material color, digital noise, compression artifacts, watermark, text, amateur
rendering.

## Note

The 6 reference SketchUp screenshots were reviewed and analyzed directly (elevation,
boundary-wall jaali zoom, large lattice screen zoom, gate zoom, planter zoom, terrace
pergola zoom) to write the material/pattern spec above, but arrived as inline chat
images with no filesystem path, so they could not be committed into this repo. If they
can be exported to files (e.g. `renders/reference/01-elevation.png`,
`02-jaali-zoom.png`, etc.), add them here so they can be attached directly to the
rendering tool alongside this brief.
