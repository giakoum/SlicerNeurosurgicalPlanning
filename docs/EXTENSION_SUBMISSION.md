# Slicer Extensions Index submission checklist

Current source baseline: **v0.6.84** (module source and UI unchanged).

## Completed

- Public repository: https://github.com/giakoum/SlicerNeurosurgicalPlanning
- Root CMake extension metadata and scripted-module CMake packaging
- `LICENSE.txt`, `NOTICE`, `CITATION.cff`, dependency notes, README
- Source and UI verified byte-for-byte against the original v0.6.84 tester archive
- Local Slicer 5.12.4 loading confirmed by the developer
- Mock CMake configuration (without Slicer SDK) passed
- Two de-identified illustration screenshots committed to `Documentation/Images/` and embedded in the README
- Raw 3D screenshot URL configured in `EXTENSION_SCREENSHOTURLS`
- Final extension icon and branded banner uploaded, README banner embedded, and `EXTENSION_ICONURL` configured
- Draft Extensions Index JSON: [NeurosurgicalPlanning.json](ExtensionsIndex/NeurosurgicalPlanning.json)
- Official draft submission: [Slicer/ExtensionsIndex PR #2413](https://github.com/Slicer/ExtensionsIndex/pull/2413) (targets the Slicer Preview `main` branch)

## Still required before submitting the Extensions Index PR

1. Perform a **real** CMake extension configuration, build and CPack packaging using an installed matching Slicer SDK/build tree or the Slicer extension build infrastructure. The mock configuration does **not** prove that Slicer can build and package this extension.
2. Verify that the committed screenshots render correctly on GitHub and that public-use permissions are documented as appropriate.
3. Verify the extension icon URL and rendering in the actual Slicer Extensions Manager.
4. Add GitHub repository topic **`3d-slicer-extension`** via repository About settings.
5. Review the README's module description and illustrative screenshots for accuracy and clarity.
6. Verify extension behavior in a **clean** Slicer 5.12 installation, particularly optional dependencies. `EXTENSION_DEPENDS` stays `NA` while integrations are optional and guarded at runtime.
7. **Submitted as Draft PR #2413.** Await maintainer authorization of extension validation, package and lint workflows; review resulting CI findings and maintainer comments before marking the PR ready for review. Stable 5.12 inclusion is a separate follow-up after Preview review.

## Notes

- Do not publish real patient images or DICOM metadata in screenshots. Use test/example or fully anonymized data.
- Preserve the original source of v0.6.84 during this packaging pass. UI help-text cleanup can be made and tested in a separate change.
- Once the release is verified and its version tag is created, confirm the Zenodo archive and DOI.
