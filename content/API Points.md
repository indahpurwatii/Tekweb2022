## API POINTS

Berikut adalah api point yang digunakan untuk membangun portfolio saya menggunakan user dan atrikel

### User

> getAllUser()

getAllUser adalah fungsi dimana ketika hendak mengambil data dari seluruh pengguna

```
GET: /user

response:
[
    {
        "id"            : "",
        "avatar"        : "",
        "nama"          : "",
        "desc_about"    : "",
    },
    ...
]
```

> getUserById()

getUserById merupakan fungsi ketika ingin mengambil/memanggil data user berdasarkan `id`

```
GET: /user/[id]

response:
{
        "id"            : "",
        "avatar"        : "",
        "nama"          : "",
        "desc_about"    : "",
},
```

> createUser()

createUser merupakan fungsi untuk menambahkan data pengguna/user

```
POST: /user

headers:
{
    Content-type: 'application/json',
    Authorization: 'Bearer [access_token]'
}

body:
{
        "id"            : "",
        "avatar"        : "",
        "nama"          : "",
        "desc_about"    : "",
}

response:
true    // if success
false   // if failure
```

> updateUser()

updateUser merupakan fungsi ketika kita hendak mengubah sebuah data pada user tertentu

```
PUT: /user

headers:
{
    Content-type: 'application/json',
    Authorization: 'Bearer [access_token]'
}

body:
{
        "id"            : "",
        "avatar"        : "",
        "nama"          : "",
        "desc_about"    : "",
}
```

> deleteUser()

fungsi deleteUser merupakan fungsi untuk menghapus data pengguna/user dari database

```
DELETE: /user/[id]

headers:
{
    Content-type: 'application/json',
    Authorization: 'Bearer [access_token]'
}

response:
true    // if success
false   // if failure
```


## Article

> getAllArticle()

getAllArticle merupakan fungsi untuk mengambil semua data article untuk ditampilkan dari server

```
GET: /article

response:
[
    {
        "id"                    : "",
        "thumbnail"             : "",
        "title"                 : "",
        "published_at"          : "",
        "author"                : "",
        "desc"                  : "",
        "read"                  : ""
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
    "thumbnail"             : "",
    "title"                 : "",
    "published_at"          : "",
    "author"                : "",
    "desc"                  : "",
    "read"                  : ""
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
    "id"                    : "",
    "thumbnail"             : "",
    "title"                 : "",
    "published_at"          : "",
    "author"                : "",
    "desc"                  : "",
    "read"                  : ""
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
    "thumbnail"             : "",
    "title"                 : "",
    "published_at"          : "",
    "author"                : "",
    "desc"                  : "",
    "read"                  : ""
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

```mermaid
    classDiagram
        class user{
        # id: int
        + nama: string
        + jurusan: string
        + desc1: string
        + desc2: string
        + getAllUser()
        + getUserById()
        + createUser()
        + updateUser()
        + deleteUser()
    }
        class article{
            # id: int
            + thumbnail: string
            + title: string
            + published_at: string
            + author: string
            + desc: string
            + read: string
            + getAllArticle()
            + getArticleById()
            + createArticle()
            + updateArticle()
            + deleteArticle()
        }
```
