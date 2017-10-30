# SlicerTetGen
This extension makes available TetGen, a quality tetrahedral mesh generator and a 3D delaunay triangulator (http://www.tetgen.org) available in 3D Slicer.

## Installation

* Download and install a recent nightly version of 3D Slicer (https://download.slicer.org).
* Start 3D Slicer application, open the Extension Manager (menu: View / Extension manager)
* Install SlicerTetGen extension.

## Tutorial #TODO

* Start 3D Slicer
* Load your volumes (for example: switch to SampleData module and load MRBrainTumor1 and MRBrainTumor2 images)
* Switch to TetGen module (in Registration category)
* Select Fixed volume (for example: MRBrainTumor1)
* Select Moving volume (this volume will be resampled to match voxels of the Fixed volume; for example: MRBrainTumor2)
* Select Preset: `generic (all)` performs deformable registration; `generic rigid (all)` performs rigid registration
* Select "Create new Volume" for Output volume (this will be the resampled moving volume)
* Select "Create new Transform" if later you want to visualize the displacement field or apply the transform to other nodes (points, surfaces, other volumes)
* Click Apply button and wait a couple of minutes

## Visualize and save results #TODO
* To comapre Fixed volume with Output volume (registered moving volume): set Fixed volume as Foreground volume in slice viewers and fade between the Output volume and Foreground volume to see how well they are aligned.
* To display displacement field: in Transforms module, select the Output transform and in Display section enable visualization in slice and/or 3D views.
* To apply transforms to other nodes: use Transforms module (or in Data module / Transform hierarchy tab: drag-and-drop nodes under the Output transform).
* To save Output volume or transform select menu: File / Save.


<p>Advanced parameters are described <a href="http://wias-berlin.de/software/tetgen/1.5/doc/manual/manual005.html#sec%3Acmdline">here</a>.