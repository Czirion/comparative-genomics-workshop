---
layout: page
title: "Learning Guide"
---

## Workshop Structure

This Workshop is divided in 4 lessons: 
1. Introduction to the Command Line for Pangenomics.    
2. Introduction to Python.      
3. Pangenome Analysis in Prokaryotes.
4. Topological Data Analysis for Pangenomics.

The sixteen hours workshop workshop is designed for a whole weekend. Nevertheless 
it could be used as a reference manual for students learning pangenomics or TDA.
Lesson is divided in an introduction to pangenome analysis 
and some topological data analysis episodes.

<a href="{{ page.root }}/fig/01-01-01.png">
   <img src="{{ page.root }}/fig/PanWorkshopWorkflow.png" alt=" Workflow of the lessons in the episode. If you are already familiar with Python or Bash, you can skip these lessons. Once in the pangenome lesson, if you have interest in applications of mathematics and topology read the Topological Data Analysos episodes, otherwise skip them and end in the other resources final episode. " />
  </a>
  
Lessons 4 (Measuring Sequence Similarity) and lesson 5 (Clustering with BLAST Results) of Pangenome Analysis in Prokaryotes serve as an introduction to constructing a pangenome using a test set of genes rather than the complete dataset. This test or mini pangenome is utilized in the chapters of the TDA section. However, in those chapters, you will also find a link to the database of this mini pangenome in case you haven't completed these episodes.These lessons use Python, so if you are not familiar with it, you can refer to the introductory Python lesson.

Starting in Lesson 6, you will find various software tools for constructing a pangenome, each with a different purpose. You can choose to follow just one or all of these chapters to explore different approaches. Chapter 7 depends on a file obtained in Chapter 6; however, you can skip this file by replacing the first instruction in the Gene Cluster subsection with `ppanggolin cluster -p pangenome.h5 --cpu 8`. Note that if you replace this instruction, your results will differ from those in the lesson, and you will need to interpret them accordingly. Nonetheless, it is possible to skip this step.





