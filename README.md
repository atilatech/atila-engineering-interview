# Atila Engineering Interview

Some of the take home projects that are part of the Atila interview process.


You can also read the [prerequisites and tutorials document](https://docs.google.com/document/d/1B4FKYcf_wNEAdpCYMe8eMrGH7vICPGJCmDgYkVNS5ew/edit#) to help you get familiar with Atila's tech stack and projects.

## Backend Task: Python Flask Search Server

Create a [Flask](https://flask.palletsprojects.com/en/1.1.x/) server that given a search query, returns the scholarships in `/data` that matches that search term.

### Example

Note: In your actual code you should use the data in `data/scholarships.json`

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
1. The API should return all the scholarships that contain the string "engineering" 
in any of the scholarship's fields.
1. So in this example, the API will return the following response:
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


## Frontend Task: Javscript React Scholarship Viewer

Your task is to design a simple web app that does the following:

1. Display a list of scholarships found in `data/scholarships.json`. The list view should show: name, deadline, amount, image, description
1. If the user enters a search term, a subset of scholarships matching the search term is displayed
1. If the user clicks on a scholarship, they are taken to the scholarship detail page where they can see: name, deadline, amount, image, description, specific_questions, eligible_schools, eligible_programs, city, province, country. See the [Atila Science and Engineering STEM scholarship](https://atila.ca/scholarship/atila-science-and-engineering-stem-scholarship-sj1i30zi) as an example.

Note: For the searching feature, you can do this completely in the frontend. You can make any assumptions you want about how the searching logic and implementation should work.

Here's a mockup of what you will be building:

![Front end mockup](https://i.imgur.com/AYMZZ3Y.png)

## Design Task Scholarship Design

1. Pick any [Atila Direct Application Scholarship](https://atila.ca/scholarship/direct).
1. Create an Intagram carousel design to advertise the scholarship using Figma. 
  1. For example, See: [SkateBoards For Hope Design](https://www.instagram.com/p/CLKSucZsxcm/)
1. Hint: You can use [Storyset](https://storyset.com/) or any other tools you want. You can also use the [Storyset Figma Plugin](https://storyset.com/for-figma)

## Submission Instructions

- For software tasks, send your interviewer a link to your Github repo
  - If applicable, make sure you include a README.md explaining how to run your code and add any necessary comments and documentation which would make it easier to understand your code and commits)
- For design tasks, send your interviewer a link to your design in Figma
