---
layout: post
title: "Direct3D 11 Initialization and Math Library"
modified: 2015-09-06 07:37:46 -0700
tags: [yume]
image:
  feature: yume.png
comments: 
share: 
---

## Direct3D 11 Initialization

This weekend I've completed the base code for initializating a RHI.D3D 11 in this case.The base class has a lot of functions it was a lot of code..D3D11Renderer.cpp already has a thousand lines even though all it does is initializing..It is really tiresome.I'm not really sure if its the right approach to load RHI as external libraries(DLLs).OGRE does this,as far as I know Unreal doesnt include RHIs like this though.I will trust OGRE3D on this one.It kinda makes sense when thinking about multi platforms but still..After linking the d3d .DLL to the executable it, thanks to "Microsoft Symbol Services" debugging is possible too.Although it took sometime to figure out how to debug external DLLs.

## Math Library

The math library is the core of a renderer.For now I've included Vector2 Vector3 Vector4 Matrix3 Matrix4 and some other classes.It has over 5k lines.Mostly I've adapted the code from other open source Math libraries.It would take too much time if I tried to code it from scratch.

The current state of the Yume engine is, the core functionality to initialize and start rendering from a RHI is there.Only available RHI is Direct3D 11. After a while,before going into the rendering operations,commands,buckets,batches, I will implement a simple OpenGL interface too.That's it for this update.
