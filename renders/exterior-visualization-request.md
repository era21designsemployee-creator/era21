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
- **Exterior walls**: **warm greige** — soft warm gray-beige matte plaster/paint finish
  with fine stucco texture and subtle tonal variation.
- Glass balcony railings: clear low-iron glass, brushed stainless-steel/chrome posts and
  handrail.
- Wood-slat wall cladding, roof fascia, entry accent panels: warm teak/walnut, matte
  oiled finish.
- Main entry double door: dark walnut wood with brass hardware.
- Ground-floor perforated gate and louvered shutter panels: matte dark gunmetal-gray.
- Terrace/balcony flooring: light gray large-format matte porcelain tile.

## Rendering brief (final prompt)

Ultra-realistic, high-quality architectural visualization, 9:16 aspect ratio, vertical
orientation, generated as an image-to-image render that strictly preserves the exact
geometry, proportions, massing, floor layout, window and door positions, balcony
design, railing design, staircase, and pergola of the reference SketchUp model — do NOT
alter, add, remove, resize, or reinterpret any design element or proportion. Apply the
material spec above throughout, with high-end PBR materials and detailed textures.
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
windows/doors/balconies, added or removed floors, incorrect lattice pattern, white or
painted lattice, cool gray walls, plastic-looking metal, flat lighting, incorrect
material color, poorly configured artificial lighting, overly dark shadows, digital
noise, compression artifacts, presence of people, watermark, text, signature, overly
saturated colors, cloudy sky, architectural deformation, floating objects, amateur
rendering.

## Note

The 5 reference SketchUp screenshots that accompanied this request are not included in
this commit — they were shared inline in the requesting conversation and were not
accessible as files on disk to save into the repository. Add them to this folder
(e.g. `renders/reference/01-elevation.png` ...) so a rendering tool/service can use them
alongside this brief.
