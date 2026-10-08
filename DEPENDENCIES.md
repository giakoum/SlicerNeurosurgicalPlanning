# Dependencies

NeurosurgicalPlanning is a scripted 3D Slicer extension. It requires 3D Slicer and
uses Slicer-bundled VTK, Qt, CTK, NumPy, and SciPy functionality.

Optional external extensions are required only for corresponding workflows:
- SlicerANTs: ANTs registration
- SlicerElastix: Elastix registration
- SlicerVMTK: Vesselness Filtering
- HDBrainExtraction / HD-BET: MRI brain extraction (with its model dependencies)
- SurfaceWrapSolidify: CT-assisted intracranial mask workflow
- AAL3 parcellation: an externally supplied segmentation/atlas; not bundled

Optional dependencies are not redistributed in this repository. Some workflows
may be unavailable without installing their dependencies separately.

The original tester-package manifest was provisional; this list should be
revalidated on a clean Slicer installation before claiming full compatibility.
