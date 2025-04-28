# csc4140-homework-3-and-4--rasterization-solved
**TO GET THIS SOLUTION VISIT:** [CSC4140 Homework 3 and 4- Rasterization Solved](https://www.ankitcodinghub.com/product/csc4140-assignment-iii-iv-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;116881&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSC4140 Homework 3 and 4- Rasterization Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Overview

In the last assignment, you have make a great achievement to move a model to screen. This time, you will dig deeply into the rasterization! Basically, this project has 6 tasks, worth a total 130 points (30 extra points can be added if you completed a fancy additional work). The tasks are as follows:

• Draw a single color triangles (20 points + 10 extra)

• Antialiasing (20 points + 10 extra)

• Transforms (10 points)

• Barycentric coordinate (10 points)

• Barycentric coordinate (10 points)

• Texture mapping (10 points)

• Mipmapping(30 points) (10 extra included if you complete well)

The goals of your write-up are for you to (a) think about and articulate what you’ve built and learned in your own words, (b) have a write-up of the project to take away from the class. Your write-up should include:

• An overview of the project, your approach to and implementation for each of the parts, and what problems you encountered and how you solved them. Strive for clarity and succinctness.

• On each part, make sure to include the results described in the corresponding Deliverables section in addition to your explanation. If you failed to generate any results correctly, provide a brief explanation of why.

• The final (optional) part for the art competition is where you have the opportunity to be creative and individual, so be sure to provide a good description of what you were going for and how you implemented it.

• Clearly indicate any extra credit items you completed, and provide a thorough explanation and illustration for each of them.

Note, before you start to do assignment, install OpenGL using the following command:

$sudo apt update

$sudo apt install freeglut3 -dev

$sudo apt install freetype6 -dev

$sudo apt install xorg-dec libglu1 -mesa-dev

1

2

3

4

After compiling, you will get a ”draw” executable file. use it to run the given .svg files.

1 Draw a single color triangles (20 points)

Implement the function rasterize_triangle function in rasterizer.cpp.

You should:

• For each pixel, perform the point-in-triangle tests with a sample point in the center of the pixel. Sample coordinates = the integer point + (.5,.5).

• In task 2, you will implement sub-pixel supersampling, but here you should just sample once per pixel and call the fill_pixel() helper function. Follow the example in the rasterize_point function in the starter code.

• Your implementation should assume that a sample on the boundary of the triangle is to be drawn. Do make sure that none of your edges are left un-rasterized.

• Your implementation should be at least as efficient as sampling only within the bounding box of the triangle (not simply every pixel in the framebuffer).

• Your code should draw the triangle regardless of the winding order of the vertices (i.e. clockwise or counter-clockwise). Check svg/basic/test6.svg.

When finished, you should be able to render test SVG files with single-color polygons (which are triangulated into triangles elsewhere in the code before being passed to your function. Complete the given function in rasterizer.cpp.

RasterizerImp::rasterize_triangle()

1

2 Antialiasing (20 points)

Use supersampling to antialias your triangles. The sample_rate parameter in DrawRend (adjusted using the − and = keys) tells you how many samples to use per pixel.

Figure 2 shows how sampling four times per pixel produces a better result than just sampling once. The fraction of the supersamples within the triangle yields a smoother edge.

Figure 1: Supersampling

Sample at sqrt(sample_rate)∗sqrt(samplerate) grid locations distributed over the pixel area.

(sample_rate is a member variable of the RasterizerImp class)

One reasonable way to think about supersampling is simply rasterizing an image that is higher resolution, then downsampling the higher resolution image to the output resolution of the framebuffer.

The original filpixel function used in Task 1 directly draws onto the framebuffer, but for supersampling, you should draw into the sample_buffer first, filling all the subsamples corresponding to the output pixel.

To reiterate the overall pipeline of the rasterizer:

• SV GParser parses the svg file into SVG class representation.

• When rasterization starts, the renderer (DrawRend :: redraw) calls SV G :: draw.

• SV G :: draw calls the specific line / triangle / point rasterization functions to generate the image primitive by primitive.

• DrawRend :: redraw calls line rasterization to draw the square boundary.

• DrawRend :: redraw calls RasterizerImp :: resolvetoframebuffer() to translate the internal buffer of the rasterizer to the screenbuffer so the image can be displayed and written into a file.

• Clear the values in your sample buffer memory and/or framebuffer appropriately at the beginning of redrawing the frame. This is erasing the frame before you start drawing.

• Update your rasterize_triangle function to perform supersampling into your supersample buffer memory. (If you implement it with no extra memory, you will get 10 more points. Memory consumed no more than the size of the image. Explain what you did and what’s the trade-off in your report).

• At the end of rasterizing all the scene elements, you will need to populate the framebuffer from your supersamples. This is sometimes called resolving the samples into the framebuffer.

• You will likely find that points and lines stop rendering correctly after your supersampling modifications. Lines and points are not supersampled, but they still need to be drawn into the supersample buffer. Modify RasterizerImp :: fillpixel if needed to restore functionality. One way to think about this is to fill all the supersamples corresponding to the point or line with the same color, so it comes out as a single sampled pixel in the framebuffer. You do NOT need to antialias points and lines.

Complete or use the given functions.

\For managing supersample buffer memory

\in rasterizer.h and rasterizer.cpp

1

2

RasterizerImp::rasterize_triangle()

RasterizerImp::set_sample_rate()

RasterizerImp::set_framebuffer_target()

RasterizerImp::clear_buffers()

\To implement triangle supersampling rasterizer.cpp

RasterizerImp::rasterize_triangle()

RasterizerImp::fill_pixel()

\For resolving supersamples to framebuffer

RasterizerImp::resolve_to_framebuffer()

3

4

5

6

7

8

9

10

11

12

13

3 Transforms (10 points)

Implement the three transforms in the transforms.cpp file according to the SV G spec. The matrices are 3×3 because they operate in homogeneous coordinates – you can see how they will be used on instances of Vector2D by looking at the way the * operator is overloaded in the same file.

Once you’ve implemented these transforms, svg/transforms/robot.svg should render correctly, as follows:

Figure 2: Texture map (left) and Transform(right)

Complete the given functions.

translate() scale() rotate()

1

2

3

4 Barycentric coordinates (10 points)

Implement RasterizerImp :: rasterizeinterpolatedcolortriangle(…) to draw a triangle with colors defined at the vertices and interpolated across the triangle area using barycentric interpolation.

Once done, you should be able to see a color wheel in svg/basic/test7.svg(below,right).

Complete the given functions.

RasterizerImp::rasterize_interpolated_color_triangle(…)

1

Figure 3: transform

5 Pixel sampling for texture mapping (10 points)

The GUI toggles RasterizerImp’s PixelSampleMethod variable psm using the ’P’ key. When psm == P_NEAREST, you should use nearest-pixel sampling, and when psm == P_LINEAR, you should use bilinear sampling. Please do so by implementing Texture :: samplenearest and

Texture :: samplebilinear functions and calling them from RasterizerImp :: rasterize_texturedtriangle(…). This approach will allow you to reuse these functions for trilinear texture filtering in Task 6.

Now you should be able to rasterize the svg files in svg/texmap/, which rely on texture maps. Hints:

• MipLevel :: texels stores the texture image pixels in the typical RGB format described above for framebuffer pixels.

• At this part of the project, you haven’t implemented level sampling (mip-mapping) yet, so the program should default to zero-th level (full resolution).

Complete the given functions.

RasterizerImp::rasterize_textured_triangle()

Texture::sample_nearest()

Texture::sample_bilinear()

1

2

3

6 Mipmapping (20 Points)

Continue with the last task. Update RasterizerImp :: rasterize_textured_triangle(…) to support sampling different mipmap levels (MipLevel S). The GUI toggles RasterizerImp’s LevelSampleMethod variable lsm using the L key. Implement the following level sampling methods in the helper function Texture :: sample.

• When lsm == L_ZERO, you should sample from the zero-th MipLevel, as in Part 5.

• When lsm == L_NEAREST, you should compute the nearest appropriate mipmap level and pass that level as a parameter to the nearest or bilinear sample function.

In addition, implement Texture :: getlevel as a helper function. You will need ( )and

) to calculate the correct mipmap level. In order to get these values corresponding to a point (x,y)(x,y) inside a triangle, you must perform the following.

• Calculate the uv barycentric coordinates of (x,y)(x,y), (x+1,y)(x+1,y), and (x,y+1)(x,y+1) in rasterize_textured_triangle(…) as sp.p_uv, sp.p_dx_uv, and sp.p_dy_uv, assign them to a SampleParams struct sp, along with other values required by the struct, and pass sp to Texture :: get_level

• Calculate the difference vectors sp.p_dxuv − sp.p_uv and sp.p_dy_uv − sp.p_uv inside

Texture :: get_level, and finally

• Scale up the difference vectors accordingly by the width and height of the full-resolution texture image.

Notes:

• The lsm and psm variables can be set independently and interacted independently. In other words, all combinations of psm == [P_NEAREST,PLINEAR]×lsm == [LZERO,L_NEAREST,L_LINE are valid.

One way to do this is by normalizing the value returned by Texture :: getlevel by the maximum level (i.e. size of the mipmap) and have that value returned by Texture :: sample as a color. Zoom in and out of the image to see how the levels change. This is a great way to both debug your implementation as well as gain intuition about level sampling! See below for two examples, where we zoom out/in to illustrate how the computed levels change.

• Be careful do not make copies of an entire Miplevel. Make sure you always use a pointer or a reference to access the miplevel. Copying entire miplevels as arguments is extremely slow!

Complete the given functions.

RasterizerImp::rasterize_textured_triangle()

Texture::sample()

Texture::get_level()

1

2

3

7 Your Submissions

The content and quality of your write-up are extremely important, and you should make sure to at least address all the points listed below. The extra credit portions are intended for students who want to challenge themselves and explore methods beyond the fundamentals, and are not worth a large amount of points. In other words, don’t necessarily expect to use the extra credit points on these projects to make up for lost points elsewhere.

Overview Give a high-level overview of what you implemented in this project. Think about what you’ve built as a whole. Share your thoughts on what interesting things you’ve learned from completing the project.

Task 1 (20 pts + 10 extra) Walk through how you rasterize triangles in your own words. Explain how your algorithm is no worse than one that checks each sample within the bounding box of the triangle. Show a png screenshot of basic/test4.svg with the default viewing parameters and with the pixel inspector centered on an interesting part of the scene. Extra credit: Draw a triangle “A” over another triangle “B” (both with alpha channel) using z-buffer (10 pts)

Task 2 (20 pts + 10 extra) Walk through your supersampling algorithm and data structures. Why is supersampling useful? What modifications did you make to the rasterization pipeline in the process? Explain how you used supersampling to antialias your triangles. Show png screenshots of basic/test4.svg with the default viewing parameters and sample rates 1, 4, and 16 to compare them side-by-side. Position the pixel inspector over an area that showcases the effect dramatically; for example, a very skinny triangle corner. Explain why these results are observed. Extra credit:

1. If you implemented alternative antialiasing methods, describe them and include comparison pictures demonstrating the difference between your method and grid-based supersampling. (5 pts) 2. When implement supersampling, reduce the memory consumption to the same level w/o supersampling. (5 pts)

Task 3 (10 pts) Create an updated version of svg/transforms/robot.svg with cubeman doing something more interesting, like waving or running. Feel free to change his colors or proportions to suit your creativity. Save your svg file as myrobot.svg in your docs/ directory and show a png screenshot of your rendered drawing in your write-up. Explain what you were trying to do with cubeman in words.

Task 4 (10 pts) Explain barycentric coordinates in your own words and use an image to aid you in your explanation. One idea is to use a svg file that plots a single triangle with one red, one green, and one blue vertex, which should produce a smoothly blended color triangle. Show a png screenshot of svg/basic/test7.svg with default viewing parameters and sample rate 1. If you make any additional images with color gradients, include them.

Task 5 (10 pts) Explain pixel sampling in your own words and describe how you implemented it to perform texture mapping. Briefly discuss the two different pixel sampling methods, nearest and bilinear. Check out the svg files in the svg/texmap/ directory. Use the pixel inspector to find a good example of where bilinear sampling clearly defeats nearest sampling. Show and compare four png screenshots using nearest sampling at 1 sample per pixel, nearest sampling at 16 samples per pixel, bilinear sampling at 1 sample per pixel, and bilinear sampling at 16 samples per pixel. Comment on the relative differences. Discuss when there will be a large difference between the two methods and why.
