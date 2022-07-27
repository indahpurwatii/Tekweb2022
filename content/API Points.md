## API POINTS

Berikut adalah api point yang digunakan untuk membangun portfolio saya menggunakan article


## Article

> getAllArticle()

getAllArticle merupakan fungsi untuk mengambil semua data article untuk ditampilkan dari server

```
GET: /article

response:
[
    {
        "id"                    : "",
        "thumbnail_url"         : "",
        "title"                 : "",
        "content"               : "",
    }
    ...
]
```

> getArticleById()

getArticleById merupakan fungsi untuk mengambil data article berdasarkan `id` tertentu

```
GET: /article/[id]

response:
{
    "id"                    : "",
    "thumbnail_url"         : "",
    "title"                 : "",
    "content"               : "",
}
```

> createArticle()

createArticle merupakan fungsi untuk membuat data article baru yang akan disimpan pada server database

```
POST: /article

headers:
{
    Content-type: 'application/json',
    Authorization: 'Bearer [access_token]'
}

body:
{
    "thumbnail_url"         : "",
    "title"                 : "",
    "content"               : "",
}

response:
true    // if success
false   // if failure
```

> updateArticle()

updateArticle merupakan fungsi untuk mengubah data pada article

```
PUT: /article

headers:
{
    Content-type: 'application/json',
    Authorization: 'Bearer [access_token]'
}

body:
{
    "id"                    : "",
    "thumbnail_url"         : "",
    "title"                 : "",
    "content"               : "",
}

response:
true    // if success
false   // if failure
```

> deleteArticle()

deleteArticle adalah fungsi untuk menghapus article dari data server

```
DELETE: /article/[id]

headers:
{
    Content-type: 'application/json',
    Authorization: 'Bearer [access_token]'
}

response:
true    // if success
false   // if failure
```

## Desain Database

berikut adalah desain database yang digunakan untuk membangun portfolio saya

```
    class article{
        # id: int
        + thumbnail_url: string
        + title: string
        + content: string
        + getAllArticle()
        + getArticleById()
        + createArticle()
        + updateArticle()
        + deleteArticle()
    }
```
