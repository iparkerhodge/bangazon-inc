# Dog Walker - Using Query String Parameters

## Practice

1. When getting a Walker by their Id, the JSON response should have all walks that have been made by that walker if the `include=walks` query string parameter is there. i.e. `/api/walkers/1?include=walks`
1. All Owner JSON responses should have Neighborhood information include if the `include=neighborhood` query string parameter is there.
1. Provide support for filtering Walkers and Dogs by Neighboorhood by accepting a `neighborhoodId` query string parameter. Example:

   ```
   /api/walkers?neighborhoodId=1
   /api/dogs?neighborhoodId=5
   ```

1. Provide support for searching Owners by name by accepting an optional `q` query string parameter. This should implement a partial search i.e searching "ohn" should include "John Doe"

> **Hint:** Use [LIKE](https://www.techonthenet.com/sql_server/like.php) in the SQL query for pattern matching.
