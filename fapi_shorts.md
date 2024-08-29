**Query Parameter in Fast API**
```
@app.get("/items/")
async def read_items(
    q: Annotated[
        str | None, 
        Query(
            alias="item-query",
            title="Query string",
            description="Query string for the items to search in the database that have a good match",
            min_length=3,
            max_length=50,
            pattern="^fixedquery$",
            deprecated=True,
        ),
    ] = None,
):
```
