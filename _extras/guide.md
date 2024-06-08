---
layout: page
title: "Instructor Notes"
---

## Workshop Structure

This Workshop is divided in 3 lessons: 
1. Introduction to Bash.    
2. Introduction to Python.      
3. Pangenome Analysis in Prokaryotes.  

The sixteen hours workshop workshop is designed for a whole weekend. Nevertheless 
it could be used as a reference manual for students learning pangenomics or TDA.
Lesson is divided in an introduction to pangenome analysis 
and some topological data analysis episodes.

<a href="{{ page.root }}/fig/01-01-01.png">
   <img src="{{ page.root }}/fig/PanWorkshopWorkflow.png" alt=" Workflow of the lessons in the episode. If you are already familiar with Python or Bash, you can skip these lessons. Once in the pangenome lesson, if you have interest in mathematics and topology read the Topological Data Analysos episodes, otherwise skip them and end in the other resources final episode. " />
  </a>
  
# General notes for the whole workshop

## Technical tips and tricks

The parent directory of everything that we will be using during the lesson is `/home/dcuser/dc_workshop`❓. At the beginning of the workshop make sure it looks like this: 

FIXME: `tree` command of the `dc_workshop`❓ folder. 💢

* Commands with ">>" : Whenever there is a command that appends contents to a file it is possible that if the learners make a typo and then run the correct command, the resulting file will have erroneous content. So when a command like that appears ask the learners to erase the file if they made a mistake, before they repeat te command. 

## Slides
Here you can find a set of [slides](https://docs.google.com/presentation/d/1MYsxgJ8rOu4cmGQw4S9EXcRtvd8CNNlEtgzbeuBiJgE/edit#slide=id.p)
with the figures of the lesson.  
## Installation

This workshop is designed to be run on pre-imaged Amazon Web Services (AWS) instances. See the 
[Setup page](https://czirion.github.io/comparative-genomics-workshop/setup.html) for complete setup instructions. If you are
teaching these lessons, and would like an AWS instance to practice on, please contact [team@carpentries.org](mailto: team@carpentries.org).

## Common problems

✳️
This workshop introduces an analysis pipeline, where each step in that pipeline is dependent on the previous step.
If a learner gets behind, or one of the steps doesn't work for them, they may not be able to catch up with the rest of the class. 
To help ensure that all learners are able to work through the whole process, we provide the solution files. This includes all
of the output files for each step in the data processing pipeline, as well as the scripts that the learners write collaboratively
with the Instructors throughout the workshop. These files are available on the hidden `.backup_dc_workshop`directory.

Make sure to tell your helpers about the `.backup_dc_workshop` directory so that they can use these resources to help
learners catch up during the workshop. 
# Notes for the Workshop
The tree of the directories whe you download the data should look like:

If you are teaching the lesson with the CCM-UNAM server you can use this [spreadsheet](https://docs.google.com/spreadsheets/d/1uiBMjlIh3U5JufVoDl9BTncHPCmYm9GT-LHUkOwWnnU/edit#gid=0) to ask the participants to choose their user:

# Notes for the Pangenome Analysis in Prokaryotes lesson

FIXME: Add 💢
- Usar un concepto en otro contexto: Aplicar un concepto en un contexto distinto al que se enseñó puede
requerir que el estudiante haga búsquedas en internet o en los manuales del código. Por ejemplo, se puede
pedir que utilicen diferentes parámetros para modificar una gráfica previamente mostrada.

{% include links.md %}

