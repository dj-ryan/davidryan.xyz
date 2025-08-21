+++
title = "Sat-Sight"
date = 2024-01-01
template = "post.html"
draft = false

[extra]
description = "Star tracking project with computer vision, stereographic projection, and celestial coordinate systems"
+++

# Sat - Sight
# Repos
[dj-ryan/sat-sight (github.com)](https://github.com/dj-ryan/sat-sight)
[dj-ryan/sat-sight-view (github.com)](https://github.com/dj-ryan/sat-sight-vie)

# links
## Calculations
[Quadratic](https://app.quadratichq.com/file/5b0314b4-d357-4f8d-8d7e-f8d49fb0e3ab)
## Datasets
[dataset - HYG](https://www.math.uwaterloo.ca/tsp/star/hyg_data.html)
[dataset  -Yayle Bright star](http://tdc-www.harvard.edu/catalogs/bsc5.html)

[svs.gsfc.nasa.gov/4851/](https://svs.gsfc.nasa.gov/4851/)

## Rust
[Organizing code & project structure - Rust Development Classes](https://rust-classes.com/chapter_4_3)

## Formulas
[Haversine formula in Python (bearing and distance between two GPS points) - Stack Overflow](https://stackoverflow.com/questions/4913349/haversine-formula-in-python-bearing-and-distance-between-two-gps-points)
[mapping - Converting from longitude\\latitude to Cartesian coordinates - Stack Overflow](https://stackoverflow.com/questions/1185408/converting-from-longitude-latitude-to-cartesian-coordinates)
[Hash Functions and list/types of Hash functions - GeeksforGeeks](https://www.geeksforgeeks.org/hash-functions-and-list-types-of-hash-functions/)
[Program for distance between two points on earth - GeeksforGeeks](https://www.geeksforgeeks.org/program-distance-two-points-earth/)

## Godot
[Can't get set\_instance\_color to work on my MultiMesh instances - Help - Godot Forum](https://forum.godotengine.org/t/cant-get-set-instance-color-to-work-on-my-multimesh-instances/49098/2)
[gdscript - Take screenshots in Godot 4.1 Stable - Stack Overflow](https://stackoverflow.com/questions/77586404/take-screenshots-in-godot-4-1-stable)
[Using signals — Godot Engine (stable) documentation in English](https://docs.godotengine.org/en/stable/getting_started/step_by_step/signals.html)
[File paths in Godot projects — Godot Engine (stable) documentation in English](https://docs.godotengine.org/en/stable/tutorials/io/data_paths.html#:~:text=By%20default%2C%20the%20user%3A%2F%2F,the%20app_userdata%2F%5Bproject_name%5D%20folder.)

## Other concepts
OpenCV concept: [Star Recognition Using Computer Vision (OpenCV) : 11 Steps (with Pictures) - Instructables](https://www.instructables.com/Star-Recognition-Using-Computer-Vision-OpenCV/)
[36698054.pdf](https://core.ac.uk/download/pdf/36698054.pdf)
[ntrs.nasa.gov/api/citations/20200001376/downloads/20200001376.pdf](https://ntrs.nasa.gov/api/citations/20200001376/downloads/20200001376.pdf)

[Introducing SOST: An Ultra-Low-Cost Star Tracker Concept Based on a Raspberry Pi and Open-Source Astronomy Software](https://ieeexplore.ieee.org/document/9179736)

## Computer Vision
[GitHub - strawlab/strand-braid: Live, low-latency 2D and 3D tracking from single or multiple high-speed cameras](https://github.com/strawlab/strand-braid)

## Angle to Pixel
[Visual Angle - Fast, Accurate, Reliable Eye Tracking](https://www.sr-research.com/eye-tracking-blog/background/visual-angle/)

[Compiler Explorer](https://godbolt.org/z/YEGbbfW97)

## Great circle calculations
[Great-circle distance - Wikipedia](https://en.wikipedia.org/wiki/Great-circle_distance)
[mathematics - Comparing angles and working out the difference - Game Development Stack Exchange](https://gamedev.stackexchange.com/questions/4467/comparing-angles-and-working-out-the-difference)

[spherical geometry - Compute angle between two points in a sphere. - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1715008/compute-angle-between-two-points-in-a-sphere)

## Vulkan - rust - ash
[Ashen Aetna | ashen-aetna](https://hoj-senna.github.io/ashen-aetna/)

## Stereographic projection
[Stereographic projection - Wikipedia](https://en.wikipedia.org/wiki/Stereographic_projection#:~:text=The%20stereographic%20projection%20gives%20a,the%20spherical%20points%20they%20represent.)

[geometry - Stereographic Projection from an Arbitrary Point - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1207799/stereographic-projection-from-an-arbitrary-point)
[Gnomonic projection - Wikipedia](https://en.wikipedia.org/wiki/Gnomonic_projection)

[arXiv:astro-ph/0207413v1 19 Jul 2002](https://arxiv.org/pdf/astro-ph/0207413)
[Gnomonic Projections of Polycra | Desmos](https://www.desmos.com/calculator/fqqb0ah0ie)
[LAMBDA - IRAS Maps Coordinate Projections Details](https://lambda.gsfc.nasa.gov/product/iras/coordproj.html)

[22. Gnomonic projection | Eu, Mircea](https://www.neacsu.net/docs/geodesy/snyder/5-azimuthal/sect_22/)




## FITS 

[How to Use FITS Images...and What are They? • PhotographingSpace.com](https://www.photographingspace.com/how-to-use-fits/)



# Standard notations

Latitude - λ (lambda, Greek L) - Rotation around the X axis - y on cartesian - Range: (-90,90)
Longitude - φ (phi, Greek F) - Rotation around the Y axis - x on cartesian - Range: (0,360)
Heading/Orientation - θ (theta, Greek T) - Range: (0, 360)

- 𝛼![{\displaystyle \alpha }](https://wikimedia.org/api/rest_v1/media/math/render/svg/b79333175c8b3f0840bfb4ec41b8072c83ea88d3) (or 𝜑![{\displaystyle \varphi }](https://wikimedia.org/api/rest_v1/media/math/render/svg/33ee699558d09cf9d653f6351f9fda0b2f4aaa3e)) is the signed angle between the _x_ axis and the _N_ axis (_x_-convention – it could also be defined between _y_ and _N_, called _y_-convention).
- 𝛽![{\displaystyle \beta }](https://wikimedia.org/api/rest_v1/media/math/render/svg/7ed48a5e36207156fb792fa79d29925d2f7901e8) (or 𝜃![{\displaystyle \theta }](https://wikimedia.org/api/rest_v1/media/math/render/svg/6e5ab2664b422d53eb0c7df3b87e1360d75ad9af)) is the angle between the _z_ axis and the _Z_ axis.
- 𝛾![{\displaystyle \gamma }](https://wikimedia.org/api/rest_v1/media/math/render/svg/a223c880b0ce3da8f64ee33c4f0010beee400b1a) (or 𝜓![{\displaystyle \psi }](https://wikimedia.org/api/rest_v1/media/math/render/svg/45e5789e5d9c8f7c79744f43ecaaf8ba42a8553a)) is the signed angle between the _N_ axis and the _X_ axis (_x_-convention).

# Star-print ideas


- Blur the image, sum pixel values where stars should be 
- Create pairs of stars for the whole image and use them as vectors

# sat sight view



**Screenshots dir:** `C:\Users\golia\AppData\Roaming\Godot\app_userdata\Sat-sight-view\screenshots`

**Window size:** `648px x 648px`

With an orthogonal view, changing the  
Size of star - changes star size
Size of universe - changes density

Azimuth coordinates are based on the observer's position on Earth and move with the Earth as it rotates and orbits the sun. Equatorial coordinates are independent of the observer's position and always point in the same direction in the sky. [Stellarium Web Online Star Map](https://stellarium-web.org/)

**Vector**

| x   | y   | z   | ?                                 |
| --- | --- | --- | --------------------------------- |
| +   | +   | +   | Nope                              |
| -   | +   | +   | Right orientation, wrong position |
| -   | +   | -   | Nope                              |
| +   | +   | -   | Very close...                     |
| +   | -   | +   | Nope                              |

**Data parse**
[Site Unreachable](https://www.convertcsv.com/fixed-width-to-csv.htm)
```
1,4,HR|5,10,Name|15,11,DM|26,6,HD|32,6,SAO|38,4,FK5|42,1,IRflag|43,1,r_IRflag|44,1,Multiple|45,5,ADS|50,2,ADScomp|52,9,VarID|61,2,RAh1900|63,2,RAm1900|65,4,RAs19000|69,1,DE-1900|70,2,DEd1900|72,2,DEm1900|74,2,DEs1900|76,2,RAh|78,2,RAm|80,4,RAs|84,1,DE-|85,2,DEd|87,2,DEm|89,2,DEs|91,6,GLON|97,6,GLAT|103,5,Vmag|108,1,n_Vmag|109,1,u_Vmag|110,5,B-V|115,1,u_B-V|116,5,U-B|121,1,u_U-B|122,5,R-I|127,1,n_R-I|128,20,SpType|148,1,n_SpType|149,6,pmRA|155,6,pmDE|161,1,n_Parallax|162,5,Parallax|167,4,RadVel|171,4,n_RadVel|175,2,l_RotVel|177,3,RotVel|180,1,u_RotVel|181,4,Dmag|185,6,Sep|191,4,MultID|195,2,MultCnt|197,1,NoteFlag
```

**conversion of polaris**

[Polaris - Wikipedia](https://en.wikipedia.org/wiki/Polaris)




| **α UMi A**                                                                            |                                                                                   |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **[Right ascension](https://en.wikipedia.org/wiki/Right_ascension "Right ascension")** | 02h 31m 49.09s[[2]](https://en.wikipedia.org/wiki/Polaris#cite_note-hipparcos2-2) |
| **[Declination](https://en.wikipedia.org/wiki/Declination "Declination")**             | +89° 15′ 50.8″[[2]](https://en.wikipedia.org/wiki/Polaris#cite_note-hipparcos2-2) |
[RA DEC flexible converter](https://www.astrouw.edu.pl/~jskowron/ra-dec/?q=02%3A31%3A49.09+89%C2%B015%2750.8%22)
 *(accuracy ~ 1e-4 deg ~ 5 mas, J2000.0, galactic coordinates)*
123.2805417    26.4613966

[Yale Bright Star Catalog](http://tdc-www.harvard.edu/catalogs/bsc5.html):

| HR  | Name     | GLON   | GLAT  | Vmag |
| --- | -------- | ------ | ----- | ---- |
| 424 | 1Alp UMi | 123.28 | 26.46 | 2.02 |


# Concepts

## Euler angles
![Euler](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a1/Eulerangles.svg/300px-Eulerangles.svg.png)

## Spherical Cords
![spherical_cords | 300](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Kugelkoord-lokb-e.svg/240px-Kugelkoord-lokb-e.svg.png)
## Lat & Lon
![lat_n_lon | 500](https://cdn.britannica.com/04/64904-050-D2054D06/cutaway-drawing-latitude-place-longitude-sizes-angles.jpg)

## Fibonacci Lattice 

[How to evenly distribute points on a sphere more effectively than the canonical Fibonacci Lattice - Extreme Learning](https://extremelearning.com.au/how-to-evenly-distribute-points-on-a-sphere-more-effectively-than-the-canonical-fibonacci-lattice/)