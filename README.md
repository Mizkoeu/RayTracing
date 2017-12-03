# 3D_Game_Graphics
Quadrics RayTracing Homework for CG Course

Introduction:

 This is an exercise for quadrics geometry, procedural texture mapping, ray casting, ray tracing and experimenting with various materials such as plastic (phuong-blinn), metal (reflection + fresnel effect), glass (refraction). The gameplay and animations are secondary to the assignment (although still rather fun to play with).

List of Features Completed:
1. Chessboard:
  Completed, with multiple clippers (three infinite slabs) intersecting each other to make a box. The outer texture is rendered wooden with procedural noise function. The main board has checkered patterns, with diffuse shading and 20% reflection to give off the glass material feel.  

2. Pawns: Completed with cone and sphere.
    Note: Actual number of pawns are reduced to 4 so as to improve graphics performance.

3. Bishops: Completed with a see-through hole in them, with the hole's inner wall also modeled and visible.

4. Kings:
  Built from clipped quadrics, including a paraboloid for the crown. Material for the king is gold with fresnel effect implemented.

5. Queens:
  Built from clipped quadrics, including a hyperboloid for the gown. Lace-like pattern is computed in shader to discard ray hits. The body of the Queen piece thus can be seen through with a helix shaped cut.

6. Rooks:
  Built using quadrics clipped by multiple (two per quadric) clippers.

7. Sun:
  Implemented a directional light source that contributes to the illumination of all objects with non-ideal BRDFs. Objects do cast shadows on one another.

8. Gloria:
  The King pieces do have (omnidirectional, isotropic) point lights over them. It's a little obscure at first, but you can move the piece using UP,DOWN,LEFT,RIGHT arrow keys to see the point light better. Appropriate shadows are cast.

9. Silver:
  The top/crown part of the Queen pieces are rendered as silver, with pure 100% reflection on all wavelengths.

10. Gold:
  The entire King pieces are rendered as gold, with proper fresnel effect implemented.

11. Ebony and Ivory (requires Sun or Gloria):
  The pawns and rooks are all made of plastic, with diffuse + Phuong Blinn shading (different exponents).

12. Wood (requires Chessboard):
  The outer part of the chessboard is made of wood, with procedural texture mapping and proper diffuse shading.

13. Normal mapping (requires 'Ebony and Ivory' or 'Silver' or 'Gold'):
  All the pawns have Normal Mapping with the provided noise function. They all have wavy/bumpy surfaces due to the procedural noise function that disturbs the normals.

14. Environment: Completed.
  Rays that do not hit any object take their radiance from an environment map texture. A semi-spherical sky mapping is implemented (singularity can be seen from the backward direction).

15. Animations:
  #1. The King piece from the Blue team can be moved around on the chessboard with UP,DOWN,LEFT,RIGHT arrow keys; With SPACE key, the King piece flies up in the sky.
  #2. The Bishops are animated too, with F going left-forward; G going right-forward; C going left-backward; B going right-backward.

16. Stretch Goals:
  #1. Glass refraction texture is also implemented. Please see the body of the Bishops as a reference.
  #2. The Glass parts of the Bishops DO NOT cast any shadow (non-shadow caster).
