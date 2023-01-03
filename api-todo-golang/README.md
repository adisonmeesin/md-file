# สร้าง API Todo ด้วย Golang

![alt golang](https://www.freecodecamp.org/news/content/images/2021/10/golang.png)

# Schema

```json
{
    id: {
        type: Number,
        required: true
	default: Auto
    },
    title: {
        type: String,
        required: true
    },
    description: {
        type: String,
        required: true,
        default: 'N/A'
    },
    onDate: {
        type: Date,
        required: true,
        default: Date.now
    },
    cardColor: {
        type: String,
        required: true,
        default: '#cddc39'
    },
    isCompleted: {
        type: Boolean,
        required: true,
        default: false
    },
    timestamps: {
        createdOn: {
            type: Date,
            required: true,
            default: Date.now
        },
        modifiedOn: {
            type: Date,
            required: true,
            default: Date.now
        },
        completedOn: {
            type: Date,
            default: null
        }
    }
}
```

# List of route

- GET /todo

- GET /todo/:todoId

- POST /todo

```json
{
    "title": "Write Test-Cases",
    "description": "Write Test-Cases for Todo API",
    "onDate": "2019-08-16T15:47:30.889Z",
    "cardColor": "#4dd0e1"
}
```

- PUT /todo/:todoId

```
{
    "title": "UPDATED: Write Documentation",
    "description": "UPDATED: Write documentation for Todo API"
}
```

- DELETE /todo/:todoId
