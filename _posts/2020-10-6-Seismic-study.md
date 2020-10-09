---
layout: post
title: Seismic Imaging Study
date: 2020-10-06 23:13:00
description: an example of a blog post with some code
---

The book ["Illustrated Seismic Processing Volume 1: Imaging"](https://library.seg.org/doi/10.1190/1.9781560803621) has plenty discussion of seismic imaging methods.

## study notes

#### Chapter 15 Full-waveform Inversion ([FWI](https://www.slim.eos.ubc.ca/research/inversion))
- FWI is similar to migration but has some differences. FWI starting with acoustic wave equation is computational cheap compared to FWI starting with elastic wave equation (~ x50 cost). In addition, the cost increases by **a factor of 16 with a doubling of the frequency of the simulation**.
- There are a variety of FWI implementations. Some FWI
practitioners use only reflection data, others use the refraction
and turning-wave data, and still others use a
combination of data types. Some practitioners include
multiples in the data; others do not include multiples.
Some replace the elastic wave equation for the acoustic
wave equation and fit shear waves in addition to compressional
waves. 
- The following explains why many practitioners do not use **reflections** in their FWI analyses. Amplitudes of reflected waves depend on both velocity and density models because reflection coefficients are a function of a product of velocity and density (impedance). Thus, using reflected-wave data for FWI suggests that this implementation models both velocity and density.