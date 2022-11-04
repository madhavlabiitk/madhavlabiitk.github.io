# How to add/edit information to the website

## Add Publications
#### Create a new Project page for your work
1. Create a new file with format `<year>_<first_name>_<one_word_description_of_the_paper_or_presentation>.yml` in the `_data/projectpages/` folder
2. Add the following information to the file - 
    ```
    title: ""
    authors: ""
    venue: ""
    affiliations: ""
    display_image: <add an image in the images folder and refer it here> eg: "2020_puneet_saliency.png"
    abstract: ""
    contact: ""
    acknowledgements: ""
    materials:
        paper_url: ""
        bibtex: ""
    ```
3. Go to `_data/projectslist.yml` and add details about the files created in the following format - 
   ```
   - name: "<year>_<first_name>_<one_word_description_of_the_paper_or_presentation>"
     url: "projectpages/<name_from_above>"
     data: "projectpages/<name_from_above>.md"
   ```
4. Finally, go to `_pages/projectpages/` folder, create a file with format `<year>_<first_name>_<one_word_description_of_the_paper_or_presentation>.md` and add details in the following format - 
   ```
   ---
    title: ""
    nav_title: "<year>_<first_name>_<one_word_description_of_the_paper_or_presentation>"
    layout: projectpages
    sitemap: false
    permalink: /projectpages/<nav_title_as_above> 
    ---
   ```

#### Add your work to the publications list
Add a new item in the `_data/publist.yml` file in the following format - 
```
 - year: 
   title: ""
   authors: ""
   venue: ""
   paper:
     url: ""
   code:
     url: ""
   project_page: 
     url: "<year>_<first_name>_<one_word_description_of_the_paper_or_presentation>"
```
## Add Team
#### Add Current Students
1. Go to the respective file (`undergrad.yml / masters.yml / phd.yml / postdoc.yml / third_party_members.yml`) in the `_data/current_students/`folder
2. Add a new object to the list and fill in the same details as mentioned for other students, as required

#### Add Alumni
1. Go to the respective file (`undergrad.yml / masters.yml / phd.yml / postdoc.yml / third_party_members.yml / project_assistants.yml / interns.yml / external.yml`) in the `data/alumni/`folder
2. Add a new object to the list and fill in the same details as mentioned for other students, as required

## Add News and Awards
#### Add News
1. Go to `_data/news.yml` and add the news in the order of latest news first. Format as below
    ```
    - date: Dec 2020
      headline: Congratulations to Hari Chandana on being awarded the prestigious Prime Minister's Research Fellowship (PMRF)!
    ```
2. Top 13 news items from the `_data/news.yml` file are shown in the homepage. This can be changed in `_includes/news.html`
3. All news seen in the News tab of *News and Awards* section is rendered from `_pages/allnews.md`

#### Add Awards and Media Coverage
All Media and Awards are added directly to `_includes/resources/awards.html` and `_includes/resources/media.html` in the same order as to be seen on the website



