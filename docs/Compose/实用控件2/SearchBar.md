# SearchBar

![image-20230517204259150](SearchBar.assets/image-20230517204259150.png)

```kotlin
@Composable
fun SearchBar(
    modifier: Modifier = Modifier,
    query: String = "",
    onQueryChange: (String) -> Unit
) {
    TextField(
        value = query,
        onValueChange = onQueryChange,
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

@Preview(showBackground = true)
@Composable
fun SearchBarPreview() {
    var query by remember { mutableStateOf("Hello") }
    SearchBar(
        query = query,
        onQueryChange = {
            query = it
        }
    )
}
```

