cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(NeurosurgicalPlanning)

set(EXTENSION_HOMEPAGE "https://github.com/giakoum/SlicerNeurosurgicalPlanning")
set(EXTENSION_CATEGORY "Planning")
set(EXTENSION_CONTRIBUTORS "Dimitrios Giakoumettis (Saint Savvas Oncological Hospital)")
set(EXTENSION_DESCRIPTION "MRI/CT registration, segmentation, vascular reconstruction, and interactive 3D neurosurgical planning.")
set(EXTENSION_ICONURL "")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/giakoum/SlicerNeurosurgicalPlanning/main/Documentation/Images/NeurosurgicalPlanning_3D.png")
set(EXTENSION_DEPENDS "NA")

find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

add_subdirectory(SurgicalPlanning)

include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
