# atila-engineering-interview


## Python Flask Search Server

Create a [Flask](https://flask.palletsprojects.com/en/1.1.x/) server that given a search query, returns the scholarships in `/data` that matches that search term.

### Example

Suppose I have the following scholarships in my database:

```json
[
  {
    "name": "Scholarship 1",
    "description": "Scholarship 1",
    "eligible_schools": ["Western University", "University of Waterloo"],
    "eligible_programs": ["Software Engineering"]
  },
  {
    "name": "Scholarship 2",
    "description": "Scholarship for engineering students",
    "eligible_schools": [],
    "eligible_programs": []
  },
  {
    "name": "Scholarship for University of British Columbia",
    "description": "Scholarship for BC students",
    "eligible_schools": [],
    "eligible_programs": []
  }
]
```

1. If I visit the following url: `http://localhost:8000/scholarships/?q=engineering`
1. The API should return all the scholarships that contain the query string "engineering" in any of the following
fields ["name", "description", "eligible_schools", "eligible_programs"]

1. So in this example, the API will return the following response
```json
{
  "query": "engineering",
  "results": [
  {
    "name": "Scholarship 1",
    "description": "Scholarship 1",
    "eligible_schools": ["Western University", "University of Waterloo"],
    "eligible_programs": ["Software Engineering"]
  },
  {
    "name": "Scholarship 2",
    "description": "Scholarship for engineering students",
    "eligible_schools": [],
    "eligible_programs": []
  }]

}
```

1. Your code should use the data in `data/scholarships.json`
## Figma Scholarship Design

1. Pick any [Atila Direct Application Scholarship](https://atila.ca/scholarship/direct).
1. Create an Intagram carousel design to advertise the scholarship using Figma. See: [SkateBoards For Hope Design](https://www.instagram.com/p/CLKSucZsxcm/)
1. Hint: You can use [Storyset](https://storyset.com/) or any other tools you want. You can also use the [Storyset Figma Plugin](https://storyset.com/for-figma)
