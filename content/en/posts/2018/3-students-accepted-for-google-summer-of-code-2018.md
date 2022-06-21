---
title: "3 Students Accepted for Google Summer of Code 2018"
date: "2018-04-24"
---

Since 2006, we have had the opportunity for Google to sponsor students to help out with Krita. For 2018 we have 3 talented students working over the summer. Over the next few months they will be getting more familiar with the Krita code base and working on their projects. They will be blogging about their experience and what they are learning along the way. We will be sure to share any progress or information along the way.

Here is a summary of their projects and what they hope to achieve.

### Ivan Yossi - Optimize Krita Soft, Gaussian and Stamp brushes mask generation to use AVX with Vc Library

Krita digital painting app relies on quick painting response to give a natural experience. A painted line is composed of thousands of images placed one after the other. This image mask creation hast to be performed super fast as it is done thousands of times each second. If the process of applying the images on canvas is not fast enough the painting process gets compromised and the enjoyment of painting is reduced.

Optimizing the mask creation can be done using the AVX instructions sets to apply transformation in vectors of data in one step. In this case the data is the image component coordinates composing the mask. Programming AVX can be done using Vc optimization library, which manages low level optimization adaptable to the user processor features. However the data must be prepared so it optimizes effectively. Optimization has already been done on the Default brush mask engine allowing it to be as much as 5 times faster than the current Gaussian mask engine.

The project aims to improve painting performance by implementing AVX optimization code for Circular Gauss, Circular Soft, Rectangular Gaussian, Rectangular Soft Rectangular and Stamp mask.

### Michael Zhou - A Swatches Docker for Krita

This project intends to create a swatches docker for Krita. It's similar to the palette docker that's already in Krita today, but it has the following advantages:

- Users can easily add, delete, drag and drop colors to give the palette a better visual pattern so that it's easier for them to keep track of the colors.
- Users can store a palette with a work so that they can ensure the colors they use throughout a painting is consistent.
- It will have a more intuitive UI design

### Andrey Kamakin Optimize multithreading in Krita's Tile Manager

This project is about improving Krita overall performance by introducing lock-free hash table for storing tiles and improving locks described in proposal

Problem: In single threaded execution of program there is no need to monitor shared resources, because it is guaranteed that only one thread can access resource. But in multi-threaded program flow it is a common problem that resources must be shared between threads, furthermore, situations such as dirty read, etc must be excluded for normal program behavior. So the simplest solution is to use locks on table operations so that only one thread can access resources and read/write

We wish all the students the best of luck this summer!
