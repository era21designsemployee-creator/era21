# Exterior Architectural Visualization — Render Request

## Reference model

SketchUp model of a 3-story modern residential building. Reference screenshots provided
(not yet committed to this repo — see note below):

1. Full front elevation, three-quarter view, on a green lawn base, showing:
   - Ground floor: entry with paneled double door, decorative wood-slat wall panels,
     perforated metal gate/fence, driveway.
   - Upper floors: glass-and-steel balcony railings, a large diamond-lattice wood/metal
     screen (jaali) spanning the left facade, cantilevered slab balconies.
   - Roof level: rooftop terrace with a spiral staircase, wood-slat pergola/fascia trim.
2. Detail: sliding louvered gray metal storage/utility doors with lattice-panel inserts.
3. Detail: close-up of the diamond-lattice wood screen where it meets a horizontal-slat
   wall and a planter box with flowering greenery.
4. Detail: the diamond-lattice screen wrapping a building corner, adjacent to glass
   balcony railing and interior sliding doors.
5. Interior/covered terrace: tiled balcony floor, an arched lattice-wood pergola frame
   over a sectional outdoor sofa, potted plants, slatted wall cladding.

## Material spec (locked — design geometry must not change)

- **Diamond-lattice (jaali) screens** — the large facade screen on the left/corner, the
  arched pergola frame over the terrace sofa, and the matching lattice inserts on the
  ground-floor sliding shutter doors: **antique brass** metal — warm aged brass tone,
  soft satin sheen, subtle dark oxidized patina in recesses/joints.
  - **Pattern is mixed, not uniform trellis**: per the close-up reference, the jaali
    geometry itself alternates between fully open (pierced/cut-through) diamond cells and
    solid (filled) diamond cells in an irregular cluster pattern — this is a feature of
    the *modeled geometry*, not a material effect, and must render exactly as modeled.
    Do not fill in the open cells or cut open the filled cells; do not regularize the
    pattern into a uniform repeating lattice.
- **Ground-floor entrance gate**: **MS (mild steel), powder-coated finish** — matte,
  even, factory-painted coating (not raw/gunmetal metal, not glossy). Keep the gate's
  exact bar/panel/perforation design from the reference close-up unchanged; only the
  finish is powder coat.
- **Exterior walls**: **light beige** — soft, pale warm-beige matte plaster/paint finish
  with fine stucco texture and subtle tonal variation (all wall surfaces, all floors).
- Glass balcony railings: clear low-iron glass, brushed stainless-steel/chrome posts and
  handrail.
- Wood-slat wall cladding, roof fascia, entry accent panels: warm teak/walnut, matte
  oiled finish.
- Main entry double door: dark walnut wood with brass hardware.
- Ground-floor louvered shutter panels (separate from the entrance gate, see above):
  matte dark gunmetal-gray.
- Terrace/balcony flooring: light gray large-format matte porcelain tile.
- **Ceilings (every floor, including covered terrace/pergola soffits)**: wooden-look
  finish, color **RGB(131, 97, 73)** / `#836149`, laid as a **black-aluminium slatted
  false ceiling** — i.e. wood-tone slats/planks running in a linear slatted pattern,
  framed/gapped with black aluminium trim between slats. Keep the slat direction and
  layout exactly as modeled per floor; only apply this color/material treatment.

## Ground-floor entrance zone — exact geometry (a prior AI render got this wrong)

A rendered output was checked against the reference model and the entrance zone (gate +
boundary wall) came out wrong — the gate lost its louvered-and-jaali-inset structure and
turned into a generic uniform grille, the wall decorative panel was simplified, and the
nameplate text was garbled. Per the zoomed reference detail, this zone must reproduce:

- **Boundary/compound wall**: light beige matte plaster, a low wall with a horizontal
  dark band running along the face roughly a third of the way up from the base. This
  band's material is **black quartz** (dark, subtly flecked stone/composite surface,
  not flat matte paint).
- **Decorative wall panel** (left of the gate, next to the driveway): the upper-left
  portion is a diamond cross-lattice (X-in-diamond) screen in the same antique-brass
  jaali material as the main facade screen; it adjoins a narrow horizontal-slat wood
  panel and a thin planter strip with low plants set into the wall face between them.
  Keep this exact layout — lattice block + slat block + planter strip side by side —
  do not simplify it into a single uniform panel. **Construction/depth — CORRECTED**:
  the boundary wall is 9 inches thick; a 5-inch-deep recess is cut into its outer face,
  and a 4-inch-deep antique-brass jaali sits inside that recess. This means the jaali
  is set INTO a pocket recessed from the wall's outer face (recessed, not standing
  proud out in front of it), and the remaining 4 inches of solid wall stays behind the
  jaali as a visible backdrop through its open cells — the wall must NOT disappear or
  read as absent behind the lattice; it is always visible as a backing surface. This is
  the same recessed-pocket construction as the large facade jaali above.
- **Nameplate/mailbox**: a small black rectangular plaque mounted on the wall to the
  right of the decorative panel, two lines of light-colored lettering (name on top,
  unit number below). Keep it as a small dark plaque in that position — see note below
  on text rendering.
- **Entry portico columns**: square columns clad in vertical warm-wood slats, framing
  the recessed entry.
- **Entrance gate** (two-leaf swing/sliding gate, MS powder-coated, matte dark
  gunmetal-gray per the material spec above) — CORRECTED per a sharper close-up
  reference, superseding any earlier "inset window" description: **each leaf is split
  into two full-height vertical strips side by side**, not a louvered leaf with a small
  window cut into it.
  - The **outer strip** (the strip farther from the gate's center, i.e. closer to each
    wall/post) is wider and is plain **horizontal louvered slats**, matte gunmetal-gray.
  - The **inner strip** (the narrower strip closer to the gate's center, where the two
    leaves meet) is filled with a **square-grid jaali lattice** — small square cells in
    a grid, an irregular mix of solid brass/wood-tone filled squares and open/pierced
    squares (same "mixed open and filled" design language as the main facade jaali, but
    a square grid here, not a diamond grid). The two leaves' inner jaali strips sit
    directly adjacent to each other at the gate's center line.
  - So left-to-right across the full gate it reads: [louver strip] [jaali strip] |
    [jaali strip] [louver strip] — symmetric about the center gap between the two
    leaves.
  - The end gate post (away from the wall) has a slim vertical ribbed/striped light
    fixture mounted on it.

**Note on signage text**: AI image-to-image renderers are generally unreliable at
reproducing small legible text (nameplates, house numbers). If the render tool cannot
render the nameplate text cleanly, it is more important to keep it as a small dark
plaque in the correct position with a plausible dark plate + light text look than to
force legible characters — flag this to the user rather than leaving obviously garbled
text.

## Rendering brief (final prompt — copy-paste ready)

```
Ultra-realistic, high-quality architectural exterior visualization, 9:16 aspect ratio,
vertical orientation, generated as an image-to-image render from the attached reference
SketchUp model screenshots. STRICTLY PRESERVE the exact geometry, proportions, massing,
floor layout, window and door positions and sizes, balcony design, glass railing design,
rooftop spiral staircase, pergola structure, and the ground-floor entrance gate design —
do NOT alter, add, remove, resize, move, or reinterpret any design element, cut, or
proportion. This is a materials-and-lighting-only render; the geometry must match the
reference exactly.

Materials (apply exactly as specified, no substitutions):
- Diamond-lattice jaali screens (facade screen, corner wrap, pergola arch, and the
  matching lattice inserts on the ground-floor sliding shutter doors): antique brass
  metal, warm aged-brass tone, soft satin sheen, subtle dark oxidized patina in the
  recesses and joints. The lattice pattern itself is a MIX of fully open (pierced)
  diamond cells and solid (filled) diamond cells in the exact irregular cluster
  arrangement shown in the reference close-ups — do not make the pattern uniform, do
  not open the filled cells, do not fill the open cells.
- Ground-floor entrance gate: MS (mild steel) with a powder-coated finish — matte, even,
  factory-painted coating, not raw metal and not glossy. Keep the exact gate bar/panel
  design from the reference.
- Exterior walls (all floors): light beige matte plaster/paint finish with fine stucco
  texture and subtle tonal variation.
- Ceilings on every floor, including the covered terrace/pergola soffit: wooden-look
  finish in a warm mid-brown wood tone, laid as a black-aluminium slatted false ceiling
  — wood-tone slats/planks in a linear slatted pattern with black aluminium trim
  between slats, exact slat direction and layout as modeled per floor.
- Glass balcony railings: clear low-iron glass with brushed stainless-steel/chrome posts
  and handrail.
- Wood-slat wall cladding, roof fascia, and entry accent panels: warm teak/walnut, matte
  oiled finish.
- Main entry double door: dark walnut wood with brass hardware.
- Ground-floor louvered shutter panels (separate from the entrance gate): matte dark
  gunmetal-gray.
- Terrace/balcony flooring: light gray large-format matte porcelain tile.

Lighting and atmosphere: natural daylight under a clear, crystal-blue sky, sun angled to
rake across the brass lattice screens and cast rich, realistic shadow patterns onto the
light beige walls behind them. Soft fill light and gentle ambient occlusion in recessed
balcony/terrace areas so interior furniture and ceilings read naturally, not blown out
or too dark. In the foreground, plants and vegetation on the opposite side of the street
for natural framing; tall pine trees in the background. Realistic asphalt street with
professional road markings, a finished sidewalk, and modern cars integrated into the
scene.

Camera: eye-level perspective, DSLR wide-angle lens, framing and vertical composition
exactly matching the reference model view.

Rendering quality: high-end PBR materials, detailed textures, Global Illumination,
Ambient Occlusion, HDR, Ray Tracing, 8K resolution, maximum sharpness and photorealism.
```

### Negative prompt

```
Low resolution, poor quality, blurry image, unrealistic textures, geometric distortion,
changed design, altered architecture, different building layout, moved or resized
windows/doors/balconies, added or removed floors, incorrect lattice pattern, uniform or
regularized lattice (ignoring the filled-vs-open cell mix), white or painted lattice,
altered or simplified entrance gate design, raw/unpainted or glossy gate metal, dark or
cool gray walls, plastic-looking metal, wrong ceiling color, flat/unslatted or white
ceiling, flat lighting, incorrect material color, poorly configured artificial lighting,
overly dark shadows, digital noise, compression artifacts, presence of people, watermark,
text, signature, overly saturated colors, cloudy sky, architectural deformation, floating
objects, amateur rendering.
```

## Final merged prompt (user's base prompt + locked material spec)

**Revision note**: an earlier version of this prompt named specific materials for
elements the user never actually specified (wood species, hardware finish, tile type,
railing metal finish, etc.) — those were this assistant's visual guesses, not
user-confirmed facts, and the user flagged this as unwanted invention. The prompt below
now states an explicit material only for the elements the user has actually specified
(jaali, walls, gate, ceiling); every other element is instructed to keep its exact
appearance/color/material from the reference photos, with no material name asserted.

```
Ultra-realistic, high-quality architectural visualization, 9:16 aspect ratio, vertical
orientation. Image-to-image render that keeps the exact design, geometry, cuts, and
layout of the reference SketchUp model unchanged — do not alter, add, remove, resize, or
reinterpret any design element.

Materials — apply only what is specified below; for every other surface, element, or
fixture in the model (glass railings, wood-slat cladding, entry door, louvered shutter
panels, flooring, fixtures, lighting fittings, furniture, etc.), reproduce its color,
texture, and finish exactly as it appears in the reference images — do not invent,
guess, or substitute a different material for anything not listed here:
- Diamond-lattice jaali screens (facade screen, corner wrap, pergola arch, and the
  matching lattice inserts on the ground-floor sliding shutter doors): antique brass
  metal — warm aged-brass tone, soft satin sheen, subtle dark oxidized patina in the
  recesses and joints. Render the lattice pattern exactly as modeled — a mix of fully
  open/pierced diamond cells and solid/filled diamond cells, per the reference
  close-ups — do not regularize or uniform the pattern.
- Ground-floor entrance gate: MS (mild steel) with a matte powder-coated finish; exact
  bar/panel design unchanged.
- Exterior walls (all floors): light beige matte plaster finish.
- Ceilings on every floor, including the covered terrace/pergola soffit: wooden-look
  black-aluminium slatted false ceiling — wood-tone slats with black aluminium trim
  between them, exact slat layout as modeled per floor.

Ground-floor entrance zone — reproduce this exact structure, a prior render got it
wrong: the entrance gate has two leaves, and each leaf is split into two full-height
vertical strips side by side — an outer, wider strip of plain horizontal louvered
slats (matte gunmetal-gray), and an inner, narrower strip filled with a square-grid
jaali lattice pattern (small square cells, an irregular mix of solid brass/wood-tone
filled squares and open/pierced squares — same mixed open/filled design language as
the main facade jaali, but a square grid, not a diamond grid). The two leaves' inner
jaali strips sit directly adjacent to each other at the gate's center line, so the gate
reads left-to-right as: louver strip, jaali strip, jaali strip, louver strip — this is
NOT a louvered leaf with one small window cut into it, and NOT a uniform grille/mesh
gate. The end gate post has a slim vertical ribbed light fixture on it. The boundary
wall (9 inches thick) to the left of the gate has a decorative panel made of three
parts side by side: a diamond cross-lattice antique-brass jaali block, a narrow
horizontal-slat wood block, and a thin planter strip with low plants — keep these as
three distinct adjacent elements, not one merged panel. The brass jaali block sits
inside a recessed pocket cut 5 inches deep into the wall's outer face, with the jaali
itself 4 inches deep within that recess — so the jaali reads as set INTO the wall, not
standing proud out in front of it, and the remaining solid wall thickness stays clearly
visible behind the lattice as a backdrop through its open cells (the wall must never
look like it disappears behind the jaali). The horizontal dark band running along the
wall is black quartz — a dark stone/composite surface, not flat paint. A small dark
rectangular two-line nameplate plaque sits on the wall to the right of the decorative
panel, along that black quartz band; render it as a small dark plate with light
lettering in the correct position rather than an altered or oversized sign, and it is
acceptable if the exact characters are not perfectly legible.

Natural daylight illumination under a clear, crystal-blue sky, brighter and richer than
a flat daylight exposure — boost the overall lighting: all wall sconces, recessed
ceiling downlights, and pendant fixtures across every floor and the entrance should read
as visibly warm and glowing (soft warm-white glow), even though it is a daytime scene,
adding depth and richness under the balconies, pergola, and entry portico rather than
leaving those covered areas flat or dim. In the foreground, plants and vegetation
strategically positioned on the opposite side of the street to create an organic visual
closure and natural framing. In the background, tall pine trees composing the
landscape. Realistic asphalt street with professional road markings, well-finished
technical sidewalk, and modern cars integrated into the scene. Eye-level perspective
captured with a DSLR wide-angle lens. Advanced technical rendering using Global
Illumination, Ambient Occlusion, HDR, Ray Tracing, and 8K resolution for maximum
sharpness and photorealism.
```

### Negative prompt (merged)

```
Low resolution, poor quality, blurry image, unrealistic textures, geometric distortion,
changed design, altered architecture, incorrect lattice pattern, uniform or regularized
lattice, white or painted lattice, altered entrance gate design, gate rendered as a
uniform grille or mesh with no louvers, entire gate leaf covered edge-to-edge in a
single diagonal X/crosshatch lattice with no plain louvered section, gate leaves
without the louver-strip-plus-jaali-strip split, diamond-pattern jaali on the gate
instead of square-grid jaali, single small window inset instead of a full-height jaali
strip, merged or simplified boundary-wall decorative panel, missing planter strip or
lattice/slat blocks on the wall panel, jaali floating proud in front of the wall with no
wall visible behind it, wall appearing to vanish or be cut away behind the jaali, dark
band on the wall rendered as flat matte paint instead of black quartz stone texture,
oversized or relocated nameplate, raw or glossy gate metal, wrong wall color, wrong
ceiling color, flat or unslatted or white ceiling, invented or substituted materials on
unspecified elements, flat or dim lighting under
covered/shaded areas, unlit sconces or fixtures, poorly configured artificial lighting,
overly dark shadows, digital noise, compression artifacts, presence of people, watermark,
garbled or illegible large text, signature, overly saturated colors, cloudy sky,
architectural
deformation, floating objects, amateur rendering.
```

## Note

The reference SketchUp screenshots that accompanied this request (the original 5, plus a
second round of zoomed-in detail shots covering the jaali fill pattern, the ground-floor
entrance gate, a balcony/bathroom vignette, the corridor closet doors, and the terrace
pergola lounge) are not included in this commit — they were shared inline in the
requesting conversation and were not accessible as files on disk to save into the
repository. Add them to this folder (e.g. `renders/reference/01-elevation.png`,
`renders/reference/detail-jaali-fill.png`, `renders/reference/detail-gate.png`, ...) so a
rendering tool/service can use them alongside this brief.

## Status

This session cannot generate the photorealistic render itself (no image-generation tool
is available here) — this document is the locked brief to hand to whatever
image-to-image rendering tool/service will produce it (e.g. Midjourney/SD img2img,
Enscape/D5/Lumion from the actual SketchUp file, or a similar AI rendering service),
alongside the exported reference screenshots.
