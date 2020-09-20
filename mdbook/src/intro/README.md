# Introduction

This page will elaborate on the main README.md to provide greater background into 
objectives, methods, governance, and tools and more.

## Goals

We cannot rely on a small group of security researchers alone to protect our public and private
institutions. There needs to be broad-based security literacy across society to improve our 
digital hygiene before we can hope to secure our hospitals, schools and municipal governments.

### Broad participation of contributions

All views are welcome. However, passions are high with regards to some topics such as
what constitutes fake news. Any contributions which clearly demonstrate the principles 
of fact verification should be welcome. Efforts aimed largely at promoting a particular
view are not.

### Support localized pods for customization

Whether it is translating to other languages, or adapting to specific needs of and
making material more relevant to local communities, we want to support pods being
able to host their own customized versions of the learning materials.

## About mdbook

The Table of Contents (TOC) is defined by the top level SUMMARY.md file.
To support different views, create different SUMMARY.md files change the
link from the default (SUMMARY_teachers.md) view to SUMMARY_student.md or SUMMARY_parent.md 
(work in progress). Simply copy or symlink the desired view into SUMMARY.md
and regenerate the book.

Similarly, the parent directory links in a new SUMMARY_students.md would need to replace
teachers.md with students.md to generate a student's view of the book. For example, below we have
replaced the default teachers.md with students.md. The student or parent view could
also remove the lines linking teacher, researcher, parent views.

SUMMARY_student.md
```
   * [Grades 3-5](break_the_fake/Grades_3_5/student.md)
```

TODO: Compare SUMMARY_student.md and SUMMARY_teacher.md mardown and generated HTML screenshots.