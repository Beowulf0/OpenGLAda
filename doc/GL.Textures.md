---
layout : default
title : API - The package GL.Textures
packages :
  - GL.Textures
versions:
  - 2.1
weight: 5
---

# The package `GL.Textures`

This package provides types and methods for handling textures. To work with a
texture, you first need to create a unique ID for your texture by defining an object
of type `Texture_Id`. When the object is defined, a unique ID is automatically
generated and registered with OpenGL. `Texture_Id` is a controlled type that
implements reference counting. As soon as the last copy of a `Texture_Id` instance
gets destroyed, the texture associated with the ID gets freed automatically, so you
don't have to worry about memory management.

To use a texture, you have to bind it to a `Texture_Target`. Both the texture IDs
and the targets come in four flavours, with each one ID type corresponding to a
certain target type. The texture targets are singletons, meaning that for each 
target type, there is only one instance.

<table>
   <thead>
      <tr>
         <th>Texture ID type</th>
         <th>Texture target type</th>
         <th>Texture target instance</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td><code>Tex_1D_Id</code></td>
         <td><code>Tex_1D_Target</code></td>
         <td><code>Texture_1D</code></td>
      </tr>
      <tr>
         <td><code>Tex_2D_Id</code></td>
         <td><code>Tex_2D_Target</code></td>
         <td><code>Texture_2D</code></td>
      </tr>
      <tr>
         <td><code>Tex_3D_Id</code></td>
         <td><code>Tex_3D_Target</code></td>
         <td><code>Texture_3D</code></td>
      </tr>
      <tr>
         <td><code>Tex_Cube_Map_Id</code></td>
         <td><code>Tex_Cube_Map_Target</code></td>
         <td><code>Texture_Cube_Map</code></td>
      </tr>
   </tbody>
</table>

You can `Bind` a texture ID only to its corresponding texture target.

- - -

**TODO:** _Loading actual texture to IDs_

- - -

The package provides setters and getters for parameters of the texture targets.
You can look up the meaning and impact of those parameters in the corresponding
section in the [OpenGL API reference](http://www.opengl.org/sdk/docs/man/xhtml/glTexParameter.xml).