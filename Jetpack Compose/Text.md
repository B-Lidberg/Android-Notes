# Text Composable

```kts
@Composable  
fun Text(  
 text: String,  
 modifier: Modifier = Modifier,  
 color: Color = Color.Unspecified,  
 fontSize: TextUnit = TextUnit.Unspecified,  
 fontStyle: FontStyle? = null,  
 fontWeight: FontWeight? = null,  
 fontFamily: FontFamily? = null,  
 letterSpacing: TextUnit = TextUnit.Unspecified,  
 textDecoration: TextDecoration? = null,  
 textAlign: TextAlign? = null,  
 lineHeight: TextUnit = TextUnit.Unspecified,  
 overflow: TextOverflow = TextOverflow.Clip,  
 softWrap: Boolean = true,  
 maxLines: Int = Int.MAX_VALUE,  
 onTextLayout: (TextLayoutResult) -> Unit = {},  
 style: TextStyle = LocalTextStyle.current  
) {  
 Text(  
 AnnotatedString(text),  
 modifier,  
 color,  
 fontSize,  
 fontStyle,  
 fontWeight,  
 fontFamily,  
 letterSpacing,  
 textDecoration,  
 textAlign,  
 lineHeight,  
 overflow,  
 softWrap,  
 maxLines,  
 emptyMap(),  
 onTextLayout,  
 style  
 )  
}
```

Text is a central piece of any UI, and Jetpack Compose makes it easier to display or write text. Compose leverages composition of its building blocks, meaning you don’t need to overwrite properties and methods or extend big classes to have a specific [[composable]] design and logic working the way you want.

Using a string resource:
```kts
@Composable
fun StringResourceText() {  
	Text(stringResource(R.string.hello_world))
}
```

AnnotatedString has a type-safe builder to make it easy to create one:
```kts
@Composable
fun MultipleStylesInText() {
	Text(buildAnnotatedString {
		withStyle(style = SpanStyle(color = Color.Blue)
		) {                
			append("H")            
		}            
			append("ello ")
			
			withStyle(
				style = SpanStyle(fontWeight = FontWeight.Bold, color = Color.Red)
			) {   
				append("W") 
			}           
			append("orld")
		}    
	)
}
```
