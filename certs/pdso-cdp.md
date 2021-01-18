[Back to Certifications](README.md)

---

# Practical DevSecOps Certified DevSecOps Professional

> Current as of late 2020.

## Overview

The CDP course is a practical introduction to the concepts of DevSecOps. It introduces a number of DevSecOps concepts and technologies, and requires student to apply them in GitLab CI pipelines or other practical applications. There is little required of the student before taking this course, although basic familiarity with Linux environments, version control, Docker, and application security would be helpful.

According to the author, this course is intended for people with some security experience who are looking to move to DevSecOps - applying their security knowledge directly into developers' workflows. I think it is equally valuable for developers, DevOps engineers, or anyone else interested in getting into DevSecOps. If someone has a year or two of experience in the software industry and the ability to study for 1-2 hours per day they shouldn't have trouble keeping up with the course.

## Registration

* $800
* Courses only begin on weekends; you can register but can't begin during the week
* Students receive:
    * Course study materials (large PDF)
    * Ability to schedule one-on-one video conference calls with course author at the course beginning and midpoint
    * Invite to course Slack channel (does not expire after course)
* Students have 30 days of access to:
    * Cloud-based practical labs
    * Video content that mainly rehashes the written study material

## Course Topics

* DevSecOps methodology and technologies
* Software Composition Analysis
* Static Application Security Testing
* Dynamic Application Security Testing
* Infrastructure as Code
* Compliance as Code
* Vulnerability Management

## Study Material

The video lectures and PDF study guide provides introductions to each topic - a brief overview, some strategic explanations of how and why each technology is used, and a survey of some common tools for each category. After reading or watching each chapter the student attempts a series of practical lab exercises in the provided cloud-based labs. A common progression of labs within a chapter include introducing the main tool being used, having the student manually implement it (ex: manually scan a local code repository then look at the results), having the student implement the tool within a GitLab CI pipeline, and having the student try out some other comparable tools.

## The Exam

You are assigned 5 challenges similar to the labs you completed during the course - note the `Exam` tag on some labs which indicates that they will be on the exam. Each challenge is somewhat more difficult than the corresponding labs - for example you may need to implement a tool that was not discussed during the course (but which is very similar to tools that were in the labs), or you may need to do a brief amount of research to explain the how and why of a given tool.

Your response to the challenges is a Word document based on a template provided by the author. For each exam challenge you need to walk a person through exactly how you solved the challenge, why each step is important, and you need to provide ample code snippets, screen shots, pipeline jobs, etc. inline with your challenge solutions. With all of the examples and step-by-step instructions, your response document will likely be one- to three-dozen pages long, or possibly more.

The exam lasts 36 hours - during the first 12 hours the student has access to the same cloud-based labs they used for the course. To solve each exam challenge the student should pick a lab that corresponds to the topic they're addressing (so that dependencies are pre-installed as necessary) and implement their solution there. While you do so, take plenty of screen shots, notes on exact commands used, copies of pipeline definitions, and all CI artifacts - these will be added to the exam solution document. After the first 12 hours have elapsed the student will lose access to the labs, but they still have an additional 24 hours to complete their response document, polish it up, and email it to the course author.
