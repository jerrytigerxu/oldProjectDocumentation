# Avantier Web Development Projects

## Search Bar Optimization (SBO)
**Objective**
- What we need
  - Search results should only contain pages and posts, and the results should be relevant and accessible
- Most important components
  - Speed and relevance
  - Flexibility and customization (filtering results and searching within specific content types)
  - Intuitive user interface (including AJAX live search)
  - Intelligent search features
  - Multilingual support and accessibility

**Development Procedure**
- Experiment with code changes on the “experimental branch” and save your actual code changes in this Trello board
- Test pushing your changes (just the php or js files) to the “dev branch” after resetting the experimental branch to match the dev branch
- Only when everyone is satisfied with the results should you update the production site

**Alpha - main filtering functionality**
- Create functionality to filter the search results based on different kinds of categories (UI development + JS interactions + Server-side PHP)
  - Resource type: case study, knowledge center, technical article, FAQ, etc.
- What needs to be created
  - UI (HTML and CSS)
  - JS to make the AJAX request (in response to UI change) and to update the HTML with the AJAX response
  - PHP to handle the AJAX request/response and to recreate the search results
- How it works
  - Sets of radio buttons under “Search Results for: [query]” that users can click on
    - Each radio button will have a value attribute that corresponds to a category slug/ID
  - The search form has a hidden input field that changes depending on the selected category
  - JS will update the search form and then send an AJAX GET request
  - PHP will then handle the request/response and recreate the search results (based on the search query and the category)
  - JS will then receive the response and update the search results on the page accordingly
- HTML/CSS → JS → PHP → JS → HTML/CSS correspond to view->controller->model->controller->view

## Consent Mode Setup (CMS)



**Action steps (TDD)**
- Project setup and requirements
  - Choose a CMP
  - Confirm GTM
  - Define requirements:
    - Consent types
    - Banner design
    - Consent language
    - Geographic scope
- Setup your tests (on testing environment)
  - Consent state
  - Banner interaction
  - Tag firing
- CMP integration and GTM configuration
  - Integrate CMP
  - Create GTM tags (CMP tag and Google Tags)
  - Create GTM triggers (consent initialization and consent update)
- Custom JS and consent logic
  - Set default consent state
  - Handle consent updates
  - Create GTM variables to store consent states and any other data needed for your consent logic
- Testing and refinement
  - Use GTM's preview mode to test your implementation
- Deployment and monitoring
  - Monitor on GTM, Google Analytics, and CMP
