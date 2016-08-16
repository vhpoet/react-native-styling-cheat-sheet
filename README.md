# React Native Styling Cheat Sheet

Most of the React Native styling material in one page. Imported from the [official docs](http://facebook.github.io/react-native/docs/getting-started.html).

![YAP](https://media.giphy.com/media/B5a9bkLouElOM/giphy.gif)

## Contents

### General
- [Flexbox](#flexbox)
- [ShadowPropTypesIOS](#shadow-prop-types-ios)
- [Transforms](#transforms)

### Components
- [Image](#image)
- [ScrollView](#scrollview)
- [Text](#text)
- [View](#view)

## Flexbox
| Name | Type | Description | 
| ---- | ---- | ----------- |
| alignItems | `customReactPropTypes.oneOf([ 'flex-start', 'flex-end', 'center', 'stretch' ])` | `alignItems` aligns children in the cross direction. For example, if children are flowing vertically, `alignItems` controls how they align horizontally. It works like `align-items` in CSS, except the default value is `stretch` instead of `flex-start`. See https://css-tricks.com/almanac/properties/a/align-items/ for more detail. |
| alignSelf | `customReactPropTypes.oneOf([ 'auto', 'flex-start', 'flex-end', 'center', 'stretch' ])` | `alignSelf` controls how a child aligns in the cross direction, overriding the `alignItems` of the parent. It works like `align-self` in CSS. See https://css-tricks.com/almanac/properties/a/align-self/ for more detail. |
| borderBottomWidth | `customReactPropTypes.number` | `borderBottomWidth` works like `border-bottom-width` in CSS. See http://www.w3schools.com/cssref/pr_border-bottom_width.asp for more details. |
| borderLeftWidth | `customReactPropTypes.number` | `borderLeftWidth` works like `border-left-width` in CSS. See http://www.w3schools.com/cssref/pr_border-bottom_width.asp for more details. |
| borderRightWidth | `customReactPropTypes.number` | `borderRightWidth` works like `border-right-width` in CSS. See http://www.w3schools.com/cssref/pr_border-right_width.asp for more details. |
| borderTopWidth | `customReactPropTypes.number` | `borderTopWidth` works like `border-top-width` in CSS. See http://www.w3schools.com/cssref/pr_border-top_width.asp for more details. |
| borderWidth | `customReactPropTypes.number` | `borderWidth` works like `border-width` in CSS. See http://www.w3schools.com/cssref/pr_border-width.asp for more details. |
| bottom | `customReactPropTypes.number` | `bottom` is the number of logical pixels to offset the bottom edge of this component. It works similarly to `bottom` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See https://developer.mozilla.org/en-US/docs/Web/CSS/bottom for more details of how `top` affects layout. |
| flex | `customReactPropTypes.number` | In React Native `flex` does not work the same way that it does in CSS. `flex` is a number rather than a string, and it works according to the `css-layout` library at https://github.com/facebook/css-layout . When `flex` is a positive number, it makes the component flexible and it will be sized proportional to its flex value. So a component with `flex` set to 2 will take twice the space as a component with `flex` set to 1. When `flex` is 0, the component is sized according to `width` and `height` and it is inflexible. When `flex` is -1, the component is normally sized according `width` and `height`. However, if there's not enough space, the component will shrink to its `minWidth` and `minHeight`. |
| flexDirection | `customReactPropTypes.oneOf([ 'row', 'row-reverse', 'column', 'column-reverse' ])` | `flexDirection` controls which directions children of a container go. `row` goes left to right, `column` goes top to bottom, and you may be able to guess what the other two do. It works like `flex-direction` in CSS, except the default is `column`. See https://css-tricks.com/almanac/properties/f/flex-direction/ for more detail. |
| flexWrap | `customReactPropTypes.oneOf([ 'wrap', 'nowrap' ])` | `flexWrap` controls whether children can wrap around after they hit the end of a flex container. It works like `flex-wrap` in CSS. See https://css-tricks.com/almanac/properties/f/flex-wrap/ for more detail. |
| height | `customReactPropTypes.number` | `height` sets the height of this component. It works similarly to `height` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See http://www.w3schools.com/cssref/pr_dim_width.asp for more details. |
| justifyContent | `customReactPropTypes.oneOf([ 'flex-start', 'flex-end', 'center', 'space-between', 'space-around' ])` | `justifyContent` aligns children in the main direction. For example, if children are flowing vertically, `justifyContent` controls how they align vertically. It works like `justify-content` in CSS. See https://css-tricks.com/almanac/properties/j/justify-content/ for more detail. |
| left | `customReactPropTypes.number` | `left` is the number of logical pixels to offset the left edge of this component. It works similarly to `left` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See https://developer.mozilla.org/en-US/docs/Web/CSS/left for more details of how `left` affects layout. |
| margin | `customReactPropTypes.number` | Setting `margin` has the same effect as setting each of `marginTop`, `marginLeft`, `marginBottom`, and `marginRight`. |
| marginBottom | `customReactPropTypes.number` | `marginBottom` works like `margin-bottom` in CSS. See http://www.w3schools.com/cssref/pr_margin-bottom.asp for more details. |
| marginHorizontal | `customReactPropTypes.number` | Setting `marginHorizontal` has the same effect as setting both `marginLeft` and `marginRight`. |
| marginLeft | `customReactPropTypes.number` | `marginLeft` works like `margin-left` in CSS. See http://www.w3schools.com/cssref/pr_margin-left.asp for more details. |
| marginRight | `customReactPropTypes.number` | `marginRight` works like `margin-right` in CSS. See http://www.w3schools.com/cssref/pr_margin-right.asp for more details. |
| marginTop | `customReactPropTypes.number` | `marginTop` works like `margin-top` in CSS. See http://www.w3schools.com/cssref/pr_margin-top.asp for more details. |
| marginVertical | `customReactPropTypes.number` | Setting `marginVertical` has the same effect as setting both `marginTop` and `marginBottom`. |
| maxHeight | `customReactPropTypes.number` | `maxHeight` is the maximum height for this component, in logical pixels. It works similarly to `max-height` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See http://www.w3schools.com/cssref/pr_dim_max-height.asp for more details. |
| maxWidth | `customReactPropTypes.number` | `maxWidth` is the maximum width for this component, in logical pixels. It works similarly to `max-width` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See http://www.w3schools.com/cssref/pr_dim_max-width.asp for more details. |
| minHeight | `customReactPropTypes.number` | `minHeight` is the minimum height for this component, in logical pixels. It works similarly to `min-height` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See http://www.w3schools.com/cssref/pr_dim_min-height.asp for more details. |
| minWidth | `customReactPropTypes.number` | `minWidth` is the minimum width for this component, in logical pixels. It works similarly to `min-width` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See http://www.w3schools.com/cssref/pr_dim_min-width.asp for more details. |
| padding | `customReactPropTypes.number` | `padding` works like `padding` in CSS. It's like setting each of `paddingTop`, `paddingBottom`, `paddingLeft`, and `paddingRight` to the same thing. See http://www.w3schools.com/css/css_padding.asp for more details. |
| paddingBottom | `customReactPropTypes.number` | `paddingBottom` works like `padding-bottom` in CSS. See http://www.w3schools.com/cssref/pr_padding-bottom.asp for more details. |
| paddingHorizontal | `customReactPropTypes.number` | Setting `paddingHorizontal` is like setting both of `paddingLeft` and `paddingRight`. |
| paddingLeft | `customReactPropTypes.number` | `paddingLeft` works like `padding-left` in CSS. See http://www.w3schools.com/cssref/pr_padding-left.asp for more details. |
| paddingRight | `customReactPropTypes.number` | `paddingRight` works like `padding-right` in CSS. See http://www.w3schools.com/cssref/pr_padding-right.asp for more details. |
| paddingTop | `customReactPropTypes.number` | `paddingTop` works like `padding-top` in CSS. See http://www.w3schools.com/cssref/pr_padding-top.asp for more details. |
| paddingVertical | `customReactPropTypes.number` | Setting `paddingVertical` is like setting both of `paddingTop` and `paddingBottom`. |
| position | `customReactPropTypes.oneOf([ 'absolute', 'relative' ])` | `position` in React Native is similar to regular CSS, but everything is set to `relative` by default, so `absolute` positioning is always just relative to the parent. If you want to position a child using specific numbers of logical pixels relative to its parent, set the child to have `absolute` position. If you want to position a child relative to something that is not its parent, just don't use styles for that. Use the component tree. See https://github.com/facebook/css-layout for more details on how `position` differs between React Native and CSS. |
| right | `customReactPropTypes.number` | `right` is the number of logical pixels to offset the right edge of this component. It works similarly to `right` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See https://developer.mozilla.org/en-US/docs/Web/CSS/right for more details of how `right` affects layout. |
| top | `customReactPropTypes.number` | `top` is the number of logical pixels to offset the top edge of this component. It works similarly to `top` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See https://developer.mozilla.org/en-US/docs/Web/CSS/top for more details of how `top` affects layout. |
| width | `customReactPropTypes.number` | `width` sets the width of this component. It works similarly to `width` in CSS, but in React Native you must use logical pixel units, rather than percents, ems, or any of that. See http://www.w3schools.com/cssref/pr_dim_width.asp for more details. |
| zIndex | `customReactPropTypes.number` | `zIndex` controls which components display on top of others. Normally, you don't use `zIndex`. Components render according to their order in the document tree, so later components draw over earlier ones. `zIndex` may be useful if you have animations or custom modal interfaces where you don't want this behavior. It works like the CSS `z-index` property - components with a larger `zIndex` will render on top. Think of the z-direction like it's pointing from the phone into your eyeball. See https://developer.mozilla.org/en-US/docs/Web/CSS/z-index for more detail. |

## Shadow Prop Types IOS
| Name | Type | Description | 
| ---- | ---- | ----------- |
| shadowColor | `customColorPropType` | Sets the drop shadow color |
| shadowOffset | `customReactPropTypes.shape( {width: ReactPropTypes.number, height: ReactPropTypes.number} )` | Sets the drop shadow offset |
| shadowOpacity | `customReactPropTypes.number` | Sets the drop shadow opacity (multiplied by the color's alpha component) |
| shadowRadius | `customReactPropTypes.number` | Sets the drop shadow blur radius |

## Transforms
| Name | Type |
| ---- | ---- |
| decomposedMatrix | `customDecomposedMatrixPropType` |
| transform | `customReactPropTypes.arrayOf( ReactPropTypes.oneOfType([ ReactPropTypes.shape({perspective: ReactPropTypes.number}), ReactPropTypes.shape({rotate: ReactPropTypes.string}), ReactPropTypes.shape({rotateX: ReactPropTypes.string}), ReactPropTypes.shape({rotateY: ReactPropTypes.string}), ReactPropTypes.shape({rotateZ: ReactPropTypes.string}), ReactPropTypes.shape({scale: ReactPropTypes.number}), ReactPropTypes.shape({scaleX: ReactPropTypes.number}), ReactPropTypes.shape({scaleY: ReactPropTypes.number}), ReactPropTypes.shape({translateX: ReactPropTypes.number}), ReactPropTypes.shape({translateY: ReactPropTypes.number}), ReactPropTypes.shape({skewX: ReactPropTypes.string}), ReactPropTypes.shape({skewY: ReactPropTypes.string}) ]) )` |
| transformMatrix | `customTransformMatrixPropType` |

## Image
| Name | Required | Type | Platforms | Description | 
| ---- | -------- | ---- | --------- | ----------- |
| ...[Flexbox](#flexbox) |
| ...[ShadowPropTypesIOS](#shadow-prop-types-ios) |
| ...[Transforms](#transforms) |
| backfaceVisibility | false | `ReactPropTypes .oneOf(['visible', 'hidden'])` | | |
| backgroundColor | false | `ColorPropType` | | |
| borderBottomLeftRadius | false | `ReactPropTypes.number` | | |
| borderBottomRightRadius | false | `ReactPropTypes.number` | | |
| borderColor | false | `ColorPropType` | | |
| borderRadius | false | `ReactPropTypes.number` | | |
| borderTopLeftRadius | false | `ReactPropTypes.number` | | |
| borderTopRightRadius | false | `ReactPropTypes.number` | | |
| borderWidth | false | `ReactPropTypes.number` | | |
| opacity | false | `ReactPropTypes.number` | | |
| overflow | false | `ReactPropTypes .oneOf(['visible', 'hidden'])` | | |
| resizeMode | false | `ReactPropTypes .oneOf(Object.keys(ImageResizeMode))` | | |
| tintColor | false | `ColorPropType` | | Changes the color of all the non-transparent pixels to the tintColor. |
| overlayColor | false | `ReactPropTypes.string` | android | When the image has rounded corners, specifying an overlayColor will cause the remaining space in the corners to be filled with a solid color. This is useful in cases which are not supported by the Android implementation of rounded corners: - Certain resize modes, such as 'contain' - Animated GIFs A typical way to use this prop is with images displayed on a solid background and setting the `overlayColor` to the same color as the background. For details of how this works under the hood, see http://frescolib.org/docs/rounded-corners-and-circles.html |

## ScrollView
| Name | Required | Type | Platforms | Description | 
| ---- | -------- | ---- | --------- | ----------- |
| ...[Flexbox](#flexbox) |
| ...[ShadowPropTypesIOS](#shadow-prop-types-ios) |
| ...[Transforms](#transforms) |
| backfaceVisibility | false | `ReactPropTypes.oneOf(['visible', 'hidden'])` | | |
| backgroundColor | false | `ColorPropType` | | |
| borderBottomColor | false | `ColorPropType` | | |
| borderBottomLeftRadius | false | `ReactPropTypes.number` | | |
| borderBottomRightRadius | false | `ReactPropTypes.number` | | |
| borderBottomWidth | false | `ReactPropTypes.number` | | |
| borderColor | false | `ColorPropType` | | |
| borderLeftColor | false | `ColorPropType` | | |
| borderLeftWidth | false | `ReactPropTypes.number` | | |
| borderRadius | false | `ReactPropTypes.number` | | |
| borderRightColor | false | `ColorPropType` | | |
| borderRightWidth | false | `ReactPropTypes.number` | | |
| borderStyle | false | `ReactPropTypes.oneOf(['solid', 'dotted', 'dashed'])` | | |
| borderTopColor | false | `ColorPropType` | | |
| borderTopLeftRadius | false | `ReactPropTypes.number` | | |
| borderTopRightRadius | false | `ReactPropTypes.number` | | |
| borderTopWidth | false | `ReactPropTypes.number` | | |
| borderWidth | false | `ReactPropTypes.number` | | |
| opacity | false | `ReactPropTypes.number` | | |
| overflow | false | `ReactPropTypes.oneOf(['visible', 'hidden'])` | | |
| elevation | false | `ReactPropTypes.number` | android | (Android-only) Sets the elevation of a view, using Android's underlying [elevation API](https://developer.android.com/training/material/shadows-clipping.html#Elevation). This adds a drop shadow to the item and affects z-order for overlapping views. Only supported on Android 5.0+, has no effect on earlier versions. |

## Text
| Name | Required | Type | Platforms | Description | 
| ---- | -------- | ---- | --------- | ----------- |
| ...[View](#view) |
| color | false | `ColorPropType` | | |
| fontFamily | false | `ReactPropTypes.string` | | |
| fontSize | false | `ReactPropTypes.number` | | |
| fontStyle | false | `ReactPropTypes.oneOf(['normal', 'italic'])` | | |
| fontWeight | false | `ReactPropTypes.oneOf( ['normal' /*default*/, 'bold', '100', '200', '300', '400', '500', '600', '700', '800', '900'] )` | | Specifies font weight. The values 'normal' and 'bold' are supported for most fonts. Not all fonts have a variant for each of the numeric values, in that case the closest one is chosen. |
| lineHeight | false | `ReactPropTypes.number` | | |
| textAlign | false | `ReactPropTypes.oneOf( ['auto' /*default*/, 'left', 'right', 'center', 'justify'] )` | | Specifies text alignment. The value 'justify' is only supported on iOS and fallbacks to `left` on Android. |
| textDecorationLine | false | `ReactPropTypes.oneOf( ['none' /*default*/, 'underline', 'line-through', 'underline line-through'] )` | | |
| textShadowColor | false | `ColorPropType` | | |
| textShadowOffset | false | `ReactPropTypes.shape( {width: ReactPropTypes.number, height: ReactPropTypes.number} )` | | |
| textShadowRadius | false | `ReactPropTypes.number` | | |
| textAlignVertical | false | `ReactPropTypes.oneOf( ['auto' /*default*/, 'top', 'bottom', 'center'] )` | android | |
| letterSpacing | false | `ReactPropTypes.number` | ios | |
| textDecorationColor | false | `ColorPropType` | ios | |
| textDecorationStyle | false | `ReactPropTypes.oneOf( ['solid' /*default*/, 'double', 'dotted','dashed'] )` | ios | |
| writingDirection | false | `ReactPropTypes.oneOf( ['auto' /*default*/, 'ltr', 'rtl'] )` | ios | |

## View
| Name | Required | Type | Platforms | Description | 
| ---- | -------- | ---- | --------- | ----------- |
| ...[Flexbox](#flexbox) |
| ...[ShadowPropTypesIOS](#shadow-prop-types-ios) |
| ...[Transforms](#transforms) |
| backfaceVisibility | false | `ReactPropTypes.oneOf(['visible', 'hidden'])` | | |
| backgroundColor | false | `ColorPropType` | | |
| borderBottomColor | false | `ColorPropType` | | |
| borderBottomLeftRadius | false | `ReactPropTypes.number` | | |
| borderBottomRightRadius | false | `ReactPropTypes.number` | | |
| borderBottomWidth | false | `ReactPropTypes.number` | | |
| borderColor | false | `ColorPropType` | | |
| borderLeftColor | false | `ColorPropType` | | |
| borderLeftWidth | false | `ReactPropTypes.number` | | |
| borderRadius | false | `ReactPropTypes.number` | | |
| borderRightColor | false | `ColorPropType` | | |
| borderRightWidth | false | `ReactPropTypes.number` | | |
| borderStyle | false | `ReactPropTypes.oneOf(['solid', 'dotted', 'dashed'])` | | |
| borderTopColor | false | `ColorPropType` | | |
| borderTopLeftRadius | false | `ReactPropTypes.number` | | |
| borderTopRightRadius | false | `ReactPropTypes.number` | | |
| borderTopWidth | false | `ReactPropTypes.number` | | |
| borderWidth | false | `ReactPropTypes.number` | | |
| opacity | false | `ReactPropTypes.number` | | |
| overflow | false | `ReactPropTypes.oneOf(['visible', 'hidden'])` | | |
| elevation | false | `ReactPropTypes.number` | android | (Android-only) Sets the elevation of a view, using Android's underlying [elevation API](https://developer.android.com/training/material/shadows-clipping.html#Elevation). This adds a drop shadow to the item and affects z-order for overlapping views. Only supported on Android 5.0+, has no effect on earlier versions. |
