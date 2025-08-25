Experiment 6 : SVG Based Drawing Application

In this experiment, I developed a simple freehand drawing tool using an SVG element as the main sketching area. The SVG behaves like a canvas where the user can draw using the mouse.

HTML Part:
I placed an <svg> element inside a container that serves as the drawing surface. Along with this, I added a heading for the experiment title and wrote my name below it for identification.

CSS Part:
To make the interface neat and user-friendly, I styled the container with padding and a border, and kept the content centered. The SVG was given a specific width, height, border, and a light background color. I also set the cursor style to crosshair, so that it feels more like a real drawing tool.

JavaScript Part:
The drawing is handled with mouse events:

On mousedown, a new <path> is created and drawing begins from the clicked point.

On mousemove, the path keeps updating by adding line segments, creating a smooth freehand effect.

On mouseup, the drawing of that particular stroke is finished and the path remains inside the SVG.

To generate strokes, I used createElementNS to insert new <path> elements into the SVG and modified their d attribute according to the mouse’s coordinates. Each stroke was styled with a blue color, stroke-width: 2px, and fill: none.

Flow of logic:

Mouse Down → Start a new path

Mouse Move → Keep extending the line

Mouse Up → Finalize the path

Conclusion:
This task gave me a clear idea of how SVG graphics, DOM manipulation, and event handling can be combined to create an interactive drawing tool inside a webpage.
