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

```
Ultra-realistic, high-quality architectural visualization, 9:16 aspect ratio, vertical
orientation. Image-to-image render that keeps the exact design, geometry, cuts, and
layout of the reference SketchUp model unchanged — do not alter, add, remove, resize, or
reinterpret any design element.

Materials: diamond-lattice jaali screens (facade screen, corner wrap, pergola arch, and
the matching lattice inserts on the ground-floor sliding shutter doors) in antique
brass metal — warm aged-brass tone, soft satin sheen, subtle dark oxidized patina in the
recesses and joints, with the lattice pattern rendered exactly as modeled (a mix of
fully open/pierced diamond cells and solid/filled diamond cells — do not regularize or
uniform the pattern). Ground-floor entrance gate in MS (mild steel) with a matte
powder-coated finish, exact bar/panel design unchanged. Exterior walls in light beige
matte plaster finish. Ceilings on every floor, including the covered terrace/pergola
soffit, in a wooden-look black-aluminium slatted false ceiling — warm wood-tone slats
with black aluminium trim between them. Glass balcony railings in clear low-iron glass
with brushed stainless-steel/chrome posts and handrail. Wood-slat wall cladding, roof
fascia, and entry accent panels in warm teak/walnut, matte oiled finish. Main entry
double door in dark walnut wood with brass hardware. Ground-floor louvered shutter
panels in matte dark gunmetal-gray. Terrace/balcony flooring in light gray large-format
matte porcelain tile. High-end PBR materials and detailed textures throughout.

Natural daylight illumination under a clear, crystal-blue sky. In the foreground, plants
and vegetation strategically positioned on the opposite side of the street to create an
organic visual closure and natural framing. In the background, tall pine trees composing
the landscape. Realistic asphalt street with professional road markings, well-finished
technical sidewalk, and modern cars integrated into the scene. Eye-level perspective
captured with a DSLR wide-angle lens. Advanced technical rendering using Global
Illumination, Ambient Occlusion, HDR, Ray Tracing, and 8K resolution for maximum
sharpness and photorealism.
```

### Negative prompt (merged)

```
Low resolution, poor quality, blurry image, unrealistic textures, geometric distortion,
changed design, altered architecture, incorrect lattice pattern, uniform or regularized
lattice, white or painted lattice, altered entrance gate design, raw or glossy gate
metal, wrong wall color, wrong ceiling color, flat or unslatted or white ceiling,
poorly configured artificial lighting, overly dark shadows, digital noise, compression
artifacts, presence of people, watermark, text, signature, overly saturated colors,
cloudy sky, architectural deformation, floating objects, amateur rendering.
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
