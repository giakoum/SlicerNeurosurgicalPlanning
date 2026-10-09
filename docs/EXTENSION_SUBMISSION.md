# Slicer Extensions Index submission checklist

Current source baseline: **v0.6.84** (module source and UI unchanged).

## Completed

- Public repository: https://github.com/giakoum/SlicerNeurosurgicalPlanning
- Root CMake extension metadata and scripted-module CMake packaging
- `LICENSE.txt`, `NOTICE`, `CITATION.cff`, dependency notes, README
- Source and UI verified byte-for-byte against the original v0.6.84 tester archive
- Local Slicer 5.12.4 loading confirmed by the developer
- Mock CMake configuration (without Slicer SDK) passed
- Draft Extensions Index JSON: [NeurosurgicalPlanning.json](ExtensionsIndex/NeurosurgicalPlanning.json)

## Still required before submitting the Extensions Index PR

1. Perform a **real** CMake extension configuration, build and CPack packaging using an installed matching Slicer SDK/build tree or the Slicer extension build infrastructure. The mock configuration does **not** prove that Slicer can build and package this extension.
2. Add at least **one informative screenshot** to the repository and README, and set its raw GitHub URL in `EXTENSION_SCREENSHOTURLS`.
3. Add an extension **icon** (PNG), host it in the repository, and set its raw GitHub URL in `EXTENSION_ICONURL`.
4. Add GitHub repository topic **`3d-slicer-extension`** via repository About settings.
5. Ensure the README clearly describes the included `SurgicalPlanning` module and includes its screenshot and documentation.
6. Verify extension behavior in a **clean** Slicer 5.12 installation, particularly optional dependencies. `EXTENSION_DEPENDS` stays `NA` while integrations are optional and guarded at runtime.
7. Submit a pull request to `Slicer/ExtensionsIndex` placing the JSON entry at the **root** of the ExtensionsIndex repository as `NeurosurgicalPlanning.json`, not under `docs/`.

## Notes

- Do not publish real patient images or DICOM metadata in screenshots. Use test/example or fully anonymized data.
- Preserve the original source of v0.6.84 during this packaging pass. UI help-text cleanup can be made and tested in a separate change.
- Once the release is verified and its version tag is created, confirm the Zenodo archive and DOI.
