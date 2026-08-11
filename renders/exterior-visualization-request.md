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
- **Exterior walls**: **warm greige** — soft warm gray-beige matte plaster/paint finish
  with fine stucco texture and subtle tonal variation.
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

## Rendering brief (final prompt)

Ultra-realistic, high-quality architectural visualization, 9:16 aspect ratio, vertical
orientation, generated as an image-to-image render that strictly preserves the exact
geometry, proportions, massing, floor layout, window and door positions, balcony
design, railing design, staircase, ground-floor entrance gate design, jaali
lattice pattern (including which cells are open vs. filled), and pergola of the
reference SketchUp model — do NOT alter, add, remove, resize, or reinterpret any design
element or proportion. Apply the material spec above throughout — including the
antique-brass jaali, MS powder-coated entrance gate, and wood-tone
(RGB 131,97,73) black-aluminium slatted false ceilings on every floor — with
high-end PBR materials and detailed textures.
Natural daylight illumination under a clear, crystal-blue sky, sun angled to rake across
the brass lattice screens and cast rich, realistic shadow patterns onto the greige walls
behind them. In the foreground, plants and vegetation positioned on the opposite side of
the street to create organic visual closure and natural framing. In the background, tall
pine trees composing the landscape. Realistic asphalt street with professional road
markings, a well-finished technical sidewalk, and modern cars integrated into the scene.
Eye-level perspective captured with a DSLR wide-angle lens. Advanced technical rendering
using Global Illumination, Ambient Occlusion, HDR, Ray Tracing, and 8K resolution for
maximum sharpness and photorealism. Camera framing and vertical composition must exactly
match the reference model view.

### Negative prompt

Low resolution, poor quality, blurry image, unrealistic textures, geometric distortion,
changed design, altered architecture, different building layout, moved or resized
windows/doors/balconies, added or removed floors, incorrect lattice pattern, uniform or
regularized lattice (ignoring the filled-vs-open cell mix), white or painted lattice,
altered or simplified entrance gate design, raw/unpainted or glossy gate metal, cool
gray walls, plastic-looking metal, wrong ceiling color, flat/unslatted or white ceiling,
flat lighting, incorrect material color, poorly configured artificial lighting, overly
dark shadows, digital noise, compression artifacts, presence of people, watermark, text,
signature, overly saturated colors, cloudy sky, architectural deformation, floating
objects, amateur rendering.

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
