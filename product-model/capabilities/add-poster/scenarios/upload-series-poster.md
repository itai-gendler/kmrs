---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Upload poster on a Series and picks an image",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "poster",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::series"
        }
      }
    },
    {
      "text": "The Product adds the image as an uploaded Poster of the Series",
      "kind": "product",
      "entities": [
        {
          "entity": "poster",
          "effect": "creates",
          "facts": [
            "Type",
            "Selected",
            "Image"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::series"
        }
      }
    }
  ]
}
---

# Upload a series poster

## Trigger

An Admin chooses Manage posters on a series and uploads an image.

## Outcome

The series has the uploaded poster among its posters.

## Edge cases

- An image over the server's Max upload size is refused.
