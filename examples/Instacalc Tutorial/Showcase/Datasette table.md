Four roadside attractions from Datasette's public demo database, and how far each is from San Francisco:

```ic
spots = import("https://latest.datasette.io/fixtures/roadside_attractions.json?_shape=array&_col=name&_col=latitude&_col=longitude") @sheet
miles = map(spots, s => 69 * sqrt((s.latitude - 37.7749)^2 + ((s.longitude + 122.4194) * cos(37.7749))^2))
nearest = round(min(miles))
farthest = round(max(miles))
bars(miles, map(spots, s => s.name))
```
