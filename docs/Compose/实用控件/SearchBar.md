# SearchBar

![image-20230330113127492](SearchBar.assets/image-20230330113127492.png)

```kotlin
@Composable
fun SearchBar(
    modifier: Modifier = Modifier
) {
    TextField(
        value = "",
        onValueChange = {},
        leadingIcon = {
            Icon(Icons.Default.Search, contentDescription = null)
        },
        placeholder = {
            Text(stringResource(id = R.string.placeholder_search))
        },
        colors = TextFieldDefaults.textFieldColors(
            backgroundColor = MaterialTheme.colors.surface
        ),
        modifier = modifier // 这里的modifier是直接在外部的操作下再做级联操作的更改
            .heightIn(min = 56.dp)
            .fillMaxWidth()
    )
}
```

```kotlin
@Preview(showBackground = true, backgroundColor = 0xFFF0EAE2)
@Composable
fun SearchBarPreview() {
    MySootheTheme { SearchBar(Modifier.padding(8.dp)) }
}
```

