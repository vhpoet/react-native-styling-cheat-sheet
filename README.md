# react-native-stylesheet-cheat-sheet

All of the React Native component styles in one page. Imported from the [official docs](http://facebook.github.io/react-native/docs/getting-started.html)

## Components
- [Image](#image-style)
- [ScrollView](#scrollview-style)
- [Text](#text-style)
- [View](#view-style)

## Image (style)
| Name | Required | Type | Platforms | Description | 
| ---- | -------- | ---- | --------- | ----------- |
| Flexbox... |
| ShadowPropTypesIOS#style... |
| Transforms... |
| backfaceVisibility | false | ReactPropTypes.oneOf(['visible', 'hidden']) | | |
| backgroundColor | false | ColorPropType | | |
| borderBottomLeftRadius | false | ReactPropTypes.number | | |
| borderBottomRightRadius | false | ReactPropTypes.number | | |
| borderColor | false | ColorPropType | | |
| borderRadius | false | ReactPropTypes.number | | |
| borderTopLeftRadius | false | ReactPropTypes.number | | |
| borderTopRightRadius | false | ReactPropTypes.number | | |
| borderWidth | false | ReactPropTypes.number | | |
| opacity | false | ReactPropTypes.number | | |
| overflow | false | ReactPropTypes.oneOf(['visible', 'hidden']) | | |
| resizeMode | false | ReactPropTypes.oneOf(Object.keys(ImageResizeMode)) | | |
| tintColor | false | ColorPropType | | Changes the color of all the non-transparent pixels to the tintColor. |
| overlayColor | false | ReactPropTypes.string | android | When the image has rounded corners, specifying an overlayColor will cause the remaining space in the corners to be filled with a solid color. This is useful in cases which are not supported by the Android implementation of rounded corners: - Certain resize modes, such as 'contain' - Animated GIFs A typical way to use this prop is with images displayed on a solid background and setting the `overlayColor` to the same color as the background. For details of how this works under the hood, see http://frescolib.org/docs/rounded-corners-and-circles.html |

## ScrollView (style)
| Name | Required | Type | Platforms | Description | 
| ---- | -------- | ---- | --------- | ----------- |
| Flexbox... |
| ShadowPropTypesIOS#style... |
| Transforms... |
| backfaceVisibility | false | ReactPropTypes.oneOf(['visible', 'hidden']) | | |
| backgroundColor | false | ColorPropType | | |
| borderBottomColor | false | ColorPropType | | |
| borderBottomLeftRadius | false | ReactPropTypes.number | | |
| borderBottomRightRadius | false | ReactPropTypes.number | | |
| borderBottomWidth | false | ReactPropTypes.number | | |
| borderColor | false | ColorPropType | | |
| borderLeftColor | false | ColorPropType | | |
| borderLeftWidth | false | ReactPropTypes.number | | |
| borderRadius | false | ReactPropTypes.number | | |
| borderRightColor | false | ColorPropType | | |
| borderRightWidth | false | ReactPropTypes.number | | |
| borderStyle | false | ReactPropTypes.oneOf(['solid', 'dotted', 'dashed']) | | |
| borderTopColor | false | ColorPropType | | |
| borderTopLeftRadius | false | ReactPropTypes.number | | |
| borderTopRightRadius | false | ReactPropTypes.number | | |
| borderTopWidth | false | ReactPropTypes.number | | |
| borderWidth | false | ReactPropTypes.number | | |
| opacity | false | ReactPropTypes.number | | |
| overflow | false | ReactPropTypes.oneOf(['visible', 'hidden']) | | |
| elevation | false | ReactPropTypes.number | android | (Android-only) Sets the elevation of a view, using Android's underlying [elevation API](https://developer.android.com/training/material/shadows-clipping.html#Elevation). This adds a drop shadow to the item and affects z-order for overlapping views. Only supported on Android 5.0+, has no effect on earlier versions. |

## Text (style)
| Name | Required | Type | Platforms | Description | 
| ---- | -------- | ---- | --------- | ----------- |
| View#style... |
| color | false | ColorPropType | | |
| fontFamily | false | ReactPropTypes.string | | |
| fontSize | false | ReactPropTypes.number | | |
| fontStyle | false | ReactPropTypes.oneOf(['normal', 'italic']) | | |
| fontWeight | false | ReactPropTypes.oneOf( ['normal' /*default*/, 'bold', '100', '200', '300', '400', '500', '600', '700', '800', '900'] ) | | Specifies font weight. The values 'normal' and 'bold' are supported for most fonts. Not all fonts have a variant for each of the numeric values, in that case the closest one is chosen. |
| lineHeight | false | ReactPropTypes.number | | |
| textAlign | false | ReactPropTypes.oneOf( ['auto' /*default*/, 'left', 'right', 'center', 'justify'] ) | | Specifies text alignment. The value 'justify' is only supported on iOS and fallbacks to `left` on Android. |
| textDecorationLine | false | ReactPropTypes.oneOf( ['none' /*default*/, 'underline', 'line-through', 'underline line-through'] ) | | |
| textShadowColor | false | ColorPropType | | |
| textShadowOffset | false | ReactPropTypes.shape( {width: ReactPropTypes.number, height: ReactPropTypes.number} ) | | |
| textShadowRadius | false | ReactPropTypes.number | | |
| textAlignVertical | false | ReactPropTypes.oneOf( ['auto' /*default*/, 'top', 'bottom', 'center'] ) | android | |
| letterSpacing | false | ReactPropTypes.number | ios | |
| textDecorationColor | false | ColorPropType | ios | |
| textDecorationStyle | false | ReactPropTypes.oneOf( ['solid' /*default*/, 'double', 'dotted','dashed'] ) | ios | |
| writingDirection | false | ReactPropTypes.oneOf( ['auto' /*default*/, 'ltr', 'rtl'] ) | ios | |

## View (style)
| Name | Required | Type | Platforms | Description | 
| ---- | -------- | ---- | --------- | ----------- |
| Flexbox... |
| ShadowPropTypesIOS#style... |
| Transforms... |
| backfaceVisibility | false | ReactPropTypes.oneOf(['visible', 'hidden']) | | |
| backgroundColor | false | ColorPropType | | |
| borderBottomColor | false | ColorPropType | | |
| borderBottomLeftRadius | false | ReactPropTypes.number | | |
| borderBottomRightRadius | false | ReactPropTypes.number | | |
| borderBottomWidth | false | ReactPropTypes.number | | |
| borderColor | false | ColorPropType | | |
| borderLeftColor | false | ColorPropType | | |
| borderLeftWidth | false | ReactPropTypes.number | | |
| borderRadius | false | ReactPropTypes.number | | |
| borderRightColor | false | ColorPropType | | |
| borderRightWidth | false | ReactPropTypes.number | | |
| borderStyle | false | ReactPropTypes.oneOf(['solid', 'dotted', 'dashed']) | | |
| borderTopColor | false | ColorPropType | | |
| borderTopLeftRadius | false | ReactPropTypes.number | | |
| borderTopRightRadius | false | ReactPropTypes.number | | |
| borderTopWidth | false | ReactPropTypes.number | | |
| borderWidth | false | ReactPropTypes.number | | |
| opacity | false | ReactPropTypes.number | | |
| overflow | false | ReactPropTypes.oneOf(['visible', 'hidden']) | | |
| elevation | false | ReactPropTypes.number | android | (Android-only) Sets the elevation of a view, using Android's underlying [elevation API](https://developer.android.com/training/material/shadows-clipping.html#Elevation). This adds a drop shadow to the item and affects z-order for overlapping views. Only supported on Android 5.0+, has no effect on earlier versions. |
