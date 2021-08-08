# TextField Composable
```kts
@Composable  
fun TextField(  
 value: TextFieldValue,  
 onValueChange: (TextFieldValue) -> Unit,  
 modifier: Modifier = Modifier,  
 enabled: Boolean = true,  
 readOnly: Boolean = false,  
 textStyle: TextStyle = LocalTextStyle.current,  
 label: @Composable (() -> Unit)? = null,  
 placeholder: @Composable (() -> Unit)? = null,  
 leadingIcon: @Composable (() -> Unit)? = null,  
 trailingIcon: @Composable (() -> Unit)? = null,  
 isError: Boolean = false,  
 visualTransformation: VisualTransformation = VisualTransformation.None,  
 keyboardOptions: KeyboardOptions = KeyboardOptions.Default,  
 keyboardActions: KeyboardActions = KeyboardActions(),  
 singleLine: Boolean = false,  
 maxLines: Int = Int.MAX_VALUE,  
 interactionSource: MutableInteractionSource = remember { MutableInteractionSource() },  
 shape: Shape =  
 MaterialTheme.shapes.small.copy(bottomEnd = ZeroCornerSize, bottomStart = ZeroCornerSize),  
 colors: TextFieldColors = TextFieldDefaults.textFieldColors()  
) {  
 TextFieldImpl(  
 type = TextFieldType.Filled,  
 enabled = enabled,  
 readOnly = readOnly,  
 value = value,  
 onValueChange = onValueChange,  
 modifier = modifier,  
 singleLine = singleLine,  
 textStyle = textStyle,  
 label = label,  
 placeholder = placeholder,  
 leading = leadingIcon,  
 trailing = trailingIcon,  
 isError = isError,  
 visualTransformation = visualTransformation,  
 keyboardOptions = keyboardOptions,  
 keyboardActions = keyboardActions,  
 maxLines = maxLines,  
 interactionSource = interactionSource,  
 shape = shape,  
 colors = colors  
 )  
}
```

Entering and modifying text
```kts
@Composable
fun SimpleFilledTextFieldSample() {
	var text by remember { mutableStateOf("Hello") }    
	TextField(
		value = text,
		onValueChange = { text = it },
		label = { Text("Label") }
	)
}
```