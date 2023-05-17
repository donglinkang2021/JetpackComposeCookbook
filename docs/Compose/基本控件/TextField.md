# TextField

```kotlin
@Composable
fun MySecondScreen() {
    ...
    val userInput = remember {
        mutableStateOf("")
    }

    Column(
        ...
    ) {
        ...
        TextField(
            value = userInput.value,
            onValueChange = { userInput.value = it },
            placeholder = { Text(text = stringResource(id = R.string.input_info)) }
        )
       ...
    }
}
```

