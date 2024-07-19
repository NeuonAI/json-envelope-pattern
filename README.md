### Wrapped JSON (Envelope Pattern)

#### Top level keys

- Hold either a document, or an array of documents
- Hold either main, or supporting documents

##### Singularity & plurality matter

To help differentiate between a single and multiple documents, a top level key
has to be named in either singular or plural noun, respectively. It intuitively
helps in maintaining consistent namings across systems.

#### Single document

```json
{
  "post": {
    "id": "post-1",
    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat.",
    "authorId": "user-a"
  },
  "users": [
    {
      "id": "user-a",
      "name": "John Doe"
    }
  ]
}
```

##### Multiple documents

```json
{
  "posts": [
    {
      "id": "post-1",
      "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat.",
      "authorId": "user-a"
    },
    {
      "id": "post-2",
      "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat.",
      "authorId": "user-b"
    },
    {
      "id": "post-3",
      "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat.",
      "authorId": "user-b"
    }
  ],
  "users": [
    {
      "id": "user-a",
      "name": "John Doe"
    },
    {
      "id": "user-b",
      "name": "Jane Smith"
    }
  ]
}
```
