# Digital Tails

Digital Tails is intended to support collaborators in extending mediasmarts.ca content.
Please visit their [Digital Literacy Framework Grades 4-6](https://mediasmarts.ca/teacher-resources/digital-literacy-framework/digital-literacy-framework-grades-4-6) for an example of the fabulous resources available.

Security researchers understand there is a need to bring better security literacy to the
general population. In this introduction, we will use a mediasmarts lesson plan for
[Break the Fake: What's real online](https://mediasmarts.ca/teacher-resources/break-fake-what%E2%80%99s-real-online) which leads students through some simple steps
that can help them identify if online content is real or fake. We will use this lesson
plan as a case study on how we hope digital-tails can enrich the mediasmarts.ca content.

The current Mediasmarts curriculum is suitable for all students. We intend to create 
extensions that are aimed at students interested in more technical skills such as
programming or data-driven journalism. The Mediasmarts domains of 
Media and Digital literacy will be enhanced with Security literacy. 


## Description

Mediasmarts has lesson plans for k-12, suitable for all students.
Mediasmarts includes the following.

**General**

* Profile of Kids in grades [4-5](https://mediasmarts.ca/sites/mediasmarts/files/pdfs/publication-report/summary/ycwwiii_trends_recommendations_profiles_4-5.pdf) or [6-7](https://mediasmarts.ca/sites/mediasmarts/files/pdfs/publication-report/summary/ycwwiii_trends_recommendations_profiles_6-7.pdf) which helps content developers understand what current skills and exposure is typical of students at this age
* [A collection of resources for parents](https://mediasmarts.ca/parents)
* [General resources for teachers](https://mediasmarts.ca/teacher-resources)
* [A broad collection of research papers](https://mediasmarts.ca/research-policy)

**Specific Topic Resources**

The resources for the specific learning activity for Break the Fake are
* [Grades 3-5 Break the Fake: What's real online?](https://mediasmarts.ca/teacher-resources/break-fake-what%E2%80%99s-real-online)
* [Grades 6-9 Break the Fake Lesson Plan: Verifying Information Online](https://mediasmarts.ca/teacher-resources/break-fake-what%E2%80%99s-real-online)

We aim to support collaborators in adding the following to enrich this content

* Student programming challenges related to the topic
* Student content development exercises for non-coding activities
* Professional research in the field, translated to the target age group
* Tools and references to support students in further explorations
    * Often these will be open source projects which may need some polishing and improvements to documentation
    * It may take the form of a researcher using the tool in a workbook to generate content relevant to current events
* Specific resources for each of the categories in the General section - Research, Teachers, Parents

This yields the following folder structure.

```
digital-tails/
   src/intro/
      /digital_privacy
      /break_the_fake
         /students
         /teachers
         /researchers
         /parents
         /administrators
         /common
       SUMMARY.md
   book/
   README.md
```

## About mdbook

The README.md describes the general purpose of the repo. 
SUMMARY.md serves as the table of contents. Content is added as GitHub markdown (.md) format
in src/ and the mdbook command creates the book/ folder in HTML format ready to be served to
browsers.

## Additional tools

To foster collaboration and distribution, we wish to support the following tools:

* mdbooks can be served on AWS LightSail or other cloud solutions as static websites for as
little as $4/month. We will add deployment scripts to automatically update the website as
changes to the repo are made (CI/CD).
* mdbooks are static. To support dynamic content such as running tools or doing coding exercises,
we will aim to support
    * Docker containers to run tools locally
    * Jupyter notebooks for interactive workbooks and lessons to be developed locally
    * Google CoLab deployments for secure hosting of Jupyter notebooks so that students only require a browser to do the exercises. See the [Twitter analytics](https://colab.research.google.com/drive/1WIcVZgbrU0DYOQqaxuaCLKY6CoLBV18O) example. (Click the "Connect" button on the top right, then start executing code cells with "Shift + Enter")

Typically we will expect researchers and technical contributors to use the local Docker environment
tools, while students and teachers will only need to interact with the GitHub repo, markdown
editors and CoLab notebooks.

## Roadmap for October

* Create the initial repo
* Contact potential collaborators in each category - Teachers, Students, Researchers, Parents, Administrators
* Create a flagship enriched lesson plan based on Break the Fake targeting 4-6 first, then other ages
* Create automated deployment template for deployment to AWS LightSail to host the mdbook
* Craete a [Jupyter book](https://blog.jupyter.org/announcing-the-new-jupyter-book-cbf7aa8bc72e
) to make the lesson plan executable in the browser rather than the current static pdf
* Create a library of containerized extension tools that highlight current research and will
support student explorations
* Create a code of conduct and copyright
* Create quizzes to assess understanding of material
* Support optional tracking of interactions to help evaluate engagement with content
* Develop a marketing campaign to increase the reach of mediasmarts materials
* Identify the next major theme to work on for November
 
After the October sprint, the above will be archived into october_sprint.md and a new
roadmap for November will replace the above.


## Getting Started

1. Clone this repo `git clone https://kbroughton/digital-tails`
2. Start the mdBook server `cd digital-tails/mdbook && mdbook serve`
3. Follow the mdbook 

### Starting mdBook Server

* Install `mdbook` with `cargo` using below command. Also binaries and other methods of installation can be found at [mdBook docs](https://github.com/rust-lang/mdBook)

```
cargo install mdbook
```

* Start mdBook to serve locally

```
cd mdbook && mdbook serve
```

* Navigate to `http://localhost:3000`

## License

* Documentation and mdbook are released under [Creative Commons Attribution Share Alike 4.0 International](CC-BY-SA-LICENSE.txt)
* Lab material including any code, script are release under [MIT License](MIT-LICENSE.txt)

## About US

Our as yet un-named organization aims to connect security professionals with educators
to cultivate security literacy.


