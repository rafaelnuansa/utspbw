## BERITA

### Create Berita (POST)
<table>
<tr>
    <td><b>URL</b></td>
    <td> {{baseURL}}/api/v1/berita </td>
</tr>
<tr>
    <td><b>Method</b></td>
    <td> POST </td>
</tr>
<tr>
    <td><b>Header</b></td>
    <td> Authorization : Bearer Token </td>
</tr>
<tr>
<td><b>Body</b></td>
<td>

``` json
{
    "judul" : "Minim dolore labore ut in voluptate quis magna est officia esse ea anim pariatur esse.",
    "deskrispsi" : "Mollit laboris dolor nulla sint. Est officia occaecat aliqua eiusmod consectetur cillum laboris adipisicing quis culpa. Fugiat tempor culpa pariatur nulla dolor elit velit.",
    "thumbnail"  : "Programming"
}
```

</td>
</tr>

<tr>
<td><b>Response Success</b></td>
<td>

``` json
{
    "status" : 201,
    "message" : "Data Berita berhasil di Input",
    "data"  : {
        "judul" : "Minim dolore labore ut in voluptate quis magna est officia esse ea anim pariatur esse.",
        "deskrispsi" : "Mollit laboris dolor nulla sint. Est officia occaecat aliqua eiusmod consectetur cillum laboris adipisicing quis culpa. Fugiat tempor culpa pariatur nulla dolor elit velit.",
        "thumbnail"  : "Programming"
    }
}

```

</td>
</tr>

<tr>
<td><b>Response Conflict</b></td>
<td>

``` json
{
    "status" : 409,
    "message" : "Data Telah digunakan",
    "data"  : {
        "value" : "Minim dolore labore ut in voluptate quis magna est officia esse ea anim pariatur esse.",
        "property" : "judul",
        "location"  : "body"
    }
}
```
</td>
</tr>
</table>

### Read Berita (GET)
<table>
<tr>
    <td><b>URL</b></td>
    <td> {{baseURL}}/api/v1/berita </td>
</tr>
<tr>
    <td><b>Method</b></td>
    <td> GET </td>
</tr>
<tr>
    <td><b>Header</b></td>
    <td> Authorization : Bearer Token </td>
</tr>

<tr>
<td><b>Response Success</b></td>
<td>

``` json
{
    "status" : 200,
    "message" : "Sukses",
    "data"  : [
        {
            "id" : 1234,
            "judul" : "Minim dolore labore ut in voluptate quis magna est officia esse ea anim pariatur esse.",
            "deskrispsi" : "Mollit laboris dolor nulla sint. Est officia occaecat aliqua eiusmod consectetur cillum laboris adipisicing quis culpa. Fugiat tempor culpa pariatur nulla dolor elit velit.",
            "thumbnail"  : "minim-dolore.jpg"
        },
        {
            "id" : 1235,
            "judul" : "Pariatur minim veniam et reprehenderit sunt cillum.",
            "deskrispsi" : "Mollit nisi mollit est cillum proident deserunt non laborum amet velit deserunt tempor culpa. Reprehenderit enim est velit enim aute eu exercitation ullamco magna culpa culpa deserunt. Consequat fugiat consequat amet et pariatur enim id aliquip duis.",
            "thumbnail"  : "pariatur-minim-veniam.jpg"
        }
    ]
}

```

</td>
</tr>
</table>


### Read Berita (GET) By Id with Query
<table>
<tr>
    <td><b>URL</b></td>
    <td> {{baseURL}}/api/v1/berita?id= </td>
</tr>
<tr>
    <td><b>Example</b></td>
    <td> {{baseURL}}/api/v1/berita?id=1234 </td>
</tr>
<tr>
    <td><b>Method</b></td>
    <td> GET </td>
</tr>
<tr>
    <td><b>Header</b></td>
    <td> Authorization : Bearer Token </td>
</tr>
<tr>
<td><b>Query</b></td>
<td> id=12345 </td>
</tr>

<tr>
<td><b>Response Success</b></td>
<td>

``` json
{
    "status" : 200,
    "message" : "Sukses",
    "data"  : {
        "id" : 1234,
        "judul" : "Minim dolore labore ut in voluptate quis magna est officia esse ea anim pariatur esse.",
        "deskrispsi" : "Mollit laboris dolor nulla sint. Est officia occaecat aliqua eiusmod consectetur cillum laboris adipisicing quis culpa. Fugiat tempor culpa pariatur nulla dolor elit velit.",
        "thumbnail"  : "minim-dolore.jpg"
    }
}

```

</td>
</tr>

<tr>
<td><b>Response Not Found</b></td>
<td>

``` json
{
    "status" : 404,
    "message" : "ID Berita Tidak ditemukan",
    "data"  : {
        "value" : "1234",
        "property" : "id",
        "location"  : "query"
    }
}
```
</td>
</tr>
</table>

### Update Berita (PUT)

<table>
<tr>
    <td><b>URL</b></td>
    <td> {{baseURL}}/api/v1/berita </td>
</tr>
<tr>
    <td><b>Method</b></td>
    <td> PUT </td>
</tr>
<tr>
    <td><b>Header</b></td>
    <td> Authorization : Bearer Token </td>
</tr>
<tr>
<td><b>Body</b></td>
<td>

``` json
{
            "id" : 1234,
            "judul" : "Minim dolore labore ut in voluptate quis magna est officia esse ea anim pariatur esse.",
            "deskrispsi" : "Mollit laboris dolor nulla sint. Est officia occaecat aliqua eiusmod consectetur cillum laboris adipisicing quis culpa. Fugiat tempor culpa pariatur nulla dolor elit velit.",
            "thumbnail"  : "minim-dolore.jpg"
}
```

</td>
</tr>

<tr>
<td><b>Response Success</b></td>
<td>

``` json
{
    "status" : 201,
    "message" : "Data Berita berhasil diupdate!",
    "data"  : {
            "id" : 1234,
            "judul" : "Minim dolore labore ut in voluptate quis magna est officia esse ea anim pariatur esse.",
            "deskrispsi" : "Mollit laboris dolor nulla sint. Est officia occaecat aliqua eiusmod consectetur cillum laboris adipisicing quis culpa. Fugiat tempor culpa pariatur nulla dolor elit velit.",
            "thumbnail"  : "minim-dolore.jpg"
    }
}

```

</td>
</tr>

<tr>
<td><b>Response Conflict</b></td>
<td>

``` json
{
    "status" : 409,
    "message" : "Data Telah digunakan",
    "data"  : {
        "value" : 1234,
        "property" : "judul",
        "location"  : "body"
    }
}
```
</td>
</tr>

<tr>
<td><b>Response Not Found</b></td>
<td>

``` json
{
    "status" : 404,
    "message" : "ID Berita Tidak ditemukan",
    "data"  : {
        "value" : 1234,
        "property" : "id",
        "location"  : "query"
    }
}
```
</td>
</tr>
</table>

### Delete Berita (DELETE)

<table>
<tr>
    <td><b>URL</b></td>
    <td> {{baseURL}}/api/v1/berita?id= </td>
</tr>
<tr>
    <td><b>Example</b></td>
    <td> {{baseURL}}/api/v1/berita?id=1234 </td>
</tr>
<tr>
    <td><b>Method</b></td>
    <td> DELETE </td>
</tr>
<tr>
    <td><b>Header</b></td>
    <td> Authorization : Bearer Token </td>
</tr>
<tr>
<td><b>Query</b></td>
<td> id=12345 </td>
</tr>

<tr>
<td><b>Response Success</b></td>
<td>

``` json
{
    "status" : 200,
    "message" : "Success Delete!",
    "data"  : [],
}

```

</td>
</tr>

<tr>
<td><b>Response Not Found</b></td>
<td>

``` json
{
    "status" : 404,
    "message" : "ID Berita Tidak ditemukan",
    "data"  : {
        "value" : "1234",
        "property" : "id",
        "location"  : "query"
    }
}
```
</td>
</tr>
</table>
