# PhotoEditor SDK - Changelog

## v5.0.4

### Changed
* Add `ADJUSTMENT_OPTIONS` to Sticker Config, allow the user the change brightness, contrast and saturation of a sticker.  

## v5.0.3

### Fixed
* Fix issues with loading gif and bmp images.
* Licensing issues.
* Filter always uses the placeholder photo. 
* Image not centered by using a custom layout.

## v5.0.2

### Fixed
* The save policy are handled correct now.
* OpenGL Error after deserialize.

### Not fixable at the moment
* Deserialization / Rendering of text is not platform independent.

## v5.0.1-RC1

**This is pre release version and can have some bugs**

### Fixed
* Problems with Android 8.0

### Changed
* Performance improvements. Preview of Brush, Sticker and Text are now extremely fast on most of the devices.
* Layer are now rendered in preview with OpenGL

### Not fixable at the moment
* Deserialization / Rendering of text is not platform independent.

## v5.0.0-beta

### Beta-Release-Notes

**This is a beta version and has some known bugs**
* Android 8.0.0 seams to have an issue with TextureView, this view is used by brush and cause display issues in preview.
  This Bug is also happen in older SDK Versions, we will hat to fix it later by changing our general implementation.
* Deserialization of text is not platform independent.
* The save policy are currently not correct.
* PNG and GIF can crash if the image is to big.

### Added
* GIF loading support for the first frame and exported as PNG or JPEG.
* Global History for all Tools, Local History for some tools.
* Support for serialization and deserialization with json schema v3.0.0 (platform independent, but with some issues).
* The background color of the editor stage is now adjustable in the LayerListSettings.
* The background color of the camera stage is now adjustable in the CameraSettings.

### Changed
* Version 2.1 of the Licence is now required. 
* Assets now must have an unique id for the serialisation.
* Method AbstractEditorTool.isRevertible() is now deprecated, please use isCancelable() and isAcceptable() instead.
* Rename imgly_icon_download to imgly_icon_save.
* Transform Tool now operates like iOS.
* Event dispatcher is now Synchronized.
* Object recycling for better performance and better thread stability.
* New thread handler for better performance and better thread stability.

### Fixed
* Errors with the Event dispatcher.
* Randomly icon change when using VectorDrawables.
* VectorDrawable display issues.
* Some short bugs.
* Add two missing default ColorFilters.

## v4.1.5

### Fixed
* Overlay with transparency looks wrong after export.
* Transform tool does not show the image, if an overlay is applied.
* Crash with NullPointerException, when call StateHandler.hasChanges().
* Crash with NullPointerException("BitmapRegionDecoder.getWidth() on a null object reference") when image format not support by tile decoder.
* Crash with IllegalStateException("child already has a parent").

### Known Bugs, but not fixable without API changes (please wait for upcoming v5.0).
* Android 8.0 has display issues while Brush (Flickering for 1 Frame).
* Some, issues with async events.
* Sometimes, the dismiss dialog is displayed without changes.

## v4.1.4

### Changed
* Remove unused ImgLyTitleBar reference. 

### Fixed
* Brush default color is transparent.

## v4.1.3

### Fixed
* Dismiss edits dialog appears without any changes.

## v4.1.2

### Changed
* Add Ability to configure existing panel options by extend panels. Simply extend a panel like `AdjustmentToolPanel` and override the `createOptionList` (returns the icons in the list) or `createQuickOptionList` (returns the icon inside the image area) method.

## v4.1.1

### Changed
* Configuration changes in PESDKConfig during the editor is open, are now updated instantly in the UI.

### Fixed
* Icon color of some icons is wrong if you change `@color/imgly_icon_color`.

## v4.1.0

### Changed
* Multiline Text feature like iOS.
* Sticker category keep the last selection.

### Fixed
* Preview of transparent images is wrong.

## v4.0.2

### Fixed
* Workaround: RenderScript crashes on Nexus devices with Android 7.1
* NullPointer exception, by some camera modules
* NullPointer exception, by a not reproduceable behavior.
* Linear Focus handles, rotate in the wrong direction if the image is flipped.
 
## v4.0.1

### Fixed
* Overlays sometimes not changed.
* Native crash on Android <= 5.0 devices, because of a memory leak inside Googles Vector Drawable support library (This is not our fault but we have found a Workaround).
* The dismiss dialog appears, without any changes.

## v4.0.0

### Changed
* OpenGl Preview for blazing fast filter preview.
* Other Performance Improvements.
* Memory Improvements.
* An improved Focus Filter.
* Smaller SDK Size
* The preview image is now automatically resized when a slider overlays the preview at the bottom, so that is always completely visible.
* Small improvements

### Added
* Tool "Overlay".
* GPS Tag Support for the Camera.
* Pinch and Zoom in Main View and Brush Tool.
* PNG export Support.

### Fixed
* A lot of bug fixes.

## v3.1.1

### Changed
* Remove old Fonts an add improved fonts.

## v3.0.15

### Fixed
* Camera crash on Androids with API lower or equal 20.
* Cutting Frames on some image size, aspect ratio combination.

## v3.0.12

### Fixed
* Small bugfixes.

## v3.0.11

### Fixed
* When dismiss dialog appears, you can still make changes to the image.
* For each time the cancel button is pressed, one new dismiss dialog is rendered on screen.
* You can also still make changes to the image during the image export.
* Icons in some special cases in wrong order.
* Sticker straighten action if the image itself is rotated.

### Changed
* Layout imgly_popup_confirm.xml has changed and is renamed to imgly_popup_confirm_dialog.xml`.
* Layout imgly_activity_photo_editor.xml has changed!

## v3.0.10

### Fixed
* Sticker list do not scroll to top if you change the category.

## v3.0.9

### Fixed
* Dismiss edits dialog appears without any changes.
* ImageDecoder crash in some constellations.
* SettingsList configurations randomly ignored.
* Force-Crop not working.
* AutoRotation is sometimes wrong.
* License validation sometimes take to long.

## v3.0.7

### Fixed
* Missing Linter Warning if you use Documents until API 19 and fix crash if you ignore this warning and use it until API 19.
* Toggled list images if you use vector and rastered drawables together.

### Changed
* Show a warning and fix wrong scaled frames, if you put the frame assets in the wrong drawable directory.
