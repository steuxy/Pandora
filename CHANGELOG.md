# Changelog

## Unreleased

## 0.5.0 (January 2021)

### Added 

- Implementation of multi scale processing for the disparity map computation. [#80]
- A `./data_sample/` directory with images and configuration files for user's first steps with Pandora [#168]
- Add extra requirements making sgm plugin available [#183]

### Changed

- Semantic change: stereo becomes matching_cost (transition name, module, files and class name). [#170]
- Merge image on input configuration section. [#169]
- Enable the use of GraphMachine if graphviz avalaible to generate machine states diagram. [#149]
- Renamed json_cheker to check_json. [#182]

### Fixed

- Confidence measure that computes the distance LR / RL in cross checking method. [#155]

## 0.4.0 (November 2020)

### Added

- Classification and segmentation maps as input. [#126]

### Changed

- Non truncation of the cost volume and the disparity map, which have the input image's size. [#152]
- Input masks convention and creation of masks dataset.

## 0.3.0 (October 2020)

### Added

- Implementation of a state machine for Pandora's sequencing management. [#107]
- Disparity grids as input to define dmin and dmax values for each pixel. [#91]
- A changelog file. [#115]

### Changed

- "Image configuration (no data of image, no data and invalid pixel of input mask ) is now
  implemented as attributes of xarray image dataset and must no longer be provided separately to the run method. [#131]
- The reference/secondary naming convention becomes left/right naming. [#135]
- Functions which can modify input arguments passed by reference does not return these references anymore. [#109]

### Fixed

- Creation of mask dataset in `read_img` function of the `img_tools` module. [#133]
- Management of no data in cbca method. [#125]
- Detection between false matches and occlusions. [#132]
