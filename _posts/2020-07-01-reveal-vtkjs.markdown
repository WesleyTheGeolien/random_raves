---
layout: post
title:  "Interactive 3D Models inside your Slideshows"
date:   2020-07-01 12:23:40 +0200
categories: Visualization
---

If a Picture is worth a thousand words then how much is a 3D model worth? Sometimes static images just don't paint the full picture, wouldn't it be great to be able to interact with your model during presentations to demonstrate key points? Try it out below.

{% include vtkElevationReader.html %}

<br>
JavaScript is gloablly used to add animation and interactivity to web sites. Fortunately [Kitware](https://www.kitware.com) have extended their Visualization ToolKit to JavaScript in the form of [vtk.js](https://kitware.github.io/vtk-js/), meaning 3D models are accessible to everyone. [Reveal.js](https://revealjs.com/), a HTML presentation framework, is going to allow us to embed the JavaScript inside out presentation.

# Reveal.js

As stated above [Reveal.js](https://revealjs.com/) is a HTML presentation Framework, a good demonstration of the power of this tool can be found on their website. Tools such as [Slides](https://slides.com) or [Jupyter Slides](https://jupyterlab.readthedocs.io/en/stable/user/export.html#reveal-js-slides) can be used for a GUI for reveal.js, it is possible to write the files directly, I have put together a template for creating single file presentations [here](https://github.com/WesleyTheGeolien/revealjs_single_file/blob/master/index.html), example below.

<iframe
    src="https://wesleythegeolien.github.io/revealjs_single_file/index.html"
    width="100%"
    height="280">
</iframe>

# VTK.js
[VTK.js](https://kitware.github.io/vtk-js/) is the JavaScript implementation of the Visualisation ToolKit. It  is currently comprimised of a subset of the C++ library however efforts are being made to port more and more tools over, to get an idea of how this framework can be used checkout [ParaView Glance](https://kitware.github.io/paraview-glance/app/).

  <iframe
      src="https://kitware.github.io/paraview-glance/app/"
      width="100%"
      height="480"
      frameborder="0"> 
  </iframe>

The example at the top of the page uses VTK.js. The official documentation shows how to use the library as a [script](https://kitware.github.io/vtk-js/examples/SimpleCone.html), in this example the [Elevation Reader Example](https://kitware.github.io/vtk-js/examples/ElevationReader.html) was adapted using the [RenderWindow Code](https://kitware.github.io/vtk-js/examples/SimpleCone.html). The code for this example can be found [here](https://github.com/WesleyTheGeolien/random_raves/blob/master/_includes/vtkElevationReader.html).

# Bringing it all together

Now that we have seen how to create a basic Reveal.js presentation and how to embed vtk.js inside a container we have all we need to make that awesome presentation! Code for the below example is [here](https://github.com/WesleyTheGeolien/revealjs_single_file/blob/master/vtkjs_elevation_reader.html).

<iframe
    src="https://wesleythegeolien.github.io/revealjs_single_file/vtkjs_elevation_reader.html"
    width="100%"
    height="480"
>
</iframe>
