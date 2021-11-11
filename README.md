# Atila Engineering Interview

Some of the take home projects that are part of the Atila interview process.


You can also read the [prerequisites and tutorials document](https://docs.google.com/document/d/1B4FKYcf_wNEAdpCYMe8eMrGH7vICPGJCmDgYkVNS5ew/edit#) to help you get familiar with Atila's tech stack and projects.

To see an open-source example of the Atila backend and frontend see:
- Atila Backend: [atila-api-demo](https://github.com/atilatech/atila-api-demo)
- Atila Frontend: [client-web-app](https://github.com/atilatech/client-web-app)

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
## Backend Task 2: Django and Django Rest Framework

1. Create a python [Django](https://www.djangoproject.com/) project that uses the [Django Rest Framework](https://www.django-rest-framework.org/) and has an API with the following two endpoints:
  1. `api/scholarships` which returns a list of scholarships
  1. `api/search/<search_term>` which returns a subset of scholarships matching the search term
1. Your application should have a `Scholarship` model

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

## Marketing Task

1. Pick any [Atila Direct Application Scholarship](https://atila.ca/scholarship/direct).
2. Make a real Twitter account and Instagram account dedicated to promoting the scholarship.
3. Add a realistic photo, bio, links, follow relevant accounts etc
4. Make a twitter thread ([example 1](https://twitter.com/atilatech/status/1446837154173394946), [example 2](https://twitter.com/atilatech/status/1404379377933107202)) and Instagram Carousel ([example 1](https://www.instagram.com/p/CTupPp5rvZr/), [example 2](https://www.instagram.com/p/CPWnK9GMYlk/)) promoting the scholarship.
5. Find 3 TikTok accounts that Atila could potentially partner with and explain why you chose them
6. Write a short writeup explaining how you created the account, what marketing strategies you used (captions, picture choice, Call to Actions etc.) and In your Google doc include links to the social media accounts, the social media posts and screenshots of your post and the 3 TikTok accounts and why you chose them
7. Send the Atila marketing team a link to the Google doc

## Submission Instructions

- For software tasks, send your interviewer a link to your Github repo
  - If applicable, make sure you include a README.md explaining how to run your code and add any necessary comments and documentation which would make it easier to understand your code and commits)
- For design tasks, send your interviewer a link to your design in Figma
- For all tasks, record a [Loom](https://www.loom.com/) video showing what you built and explaining your code
  - The video doesn't have to be anything too elaborate and long, it should be about 30-60 seconds long
  - Some things you can talk about: showing the full product flow, an interesting technical problem you faced in your code and how you solved it, ideas for how you could improve what you built
