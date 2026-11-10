Shopify Interactive Brand Section

A full-height brand statement section for a luxury menswear store. A canvas of woven threads reacts to the cursor, a large glyph is revealed inside the threads, and a row of "standards" rotates automatically until the visitor takes over.

Features
Animated thread canvas that ripples with the cursor and when a tenet is selected
Large glyph (set in the editor) revealed inside the threads
Up to 4 tenets with matching statements, auto-rotating until the visitor interacts
Pause/play control for the auto-rotation
Fully editable in the theme editor: colours, headline, subtext, glyph, tenets, footer
Accent colour setting drives the canvas threads as well as the text
Responsive layout with a mobile-specific glyph position and lighter canvas settings
Performance
The animation only runs while the section is on screen and the browser tab is visible (IntersectionObserver and the Page Visibility API)
The glyph mask is drawn once per resize, not every frame
Device pixel ratio is capped (2 on desktop, 1.5 on mobile) with fewer thread points on small screens
Resizing is handled with ResizeObserver
With prefers-reduced-motion, one static frame is rendered and auto-rotation is off
Accessibility
Tenets are real buttons with aria-pressed, and hidden statements are aria-hidden
Visible focus styles
Auto-rotation can be paused, and stops once the visitor interacts
Decorative canvas is hidden from assistive technology
Text sizes are 11px or larger
Theme editor support

The script cleans up on shopify:section:unload, so re-rendering the section in the theme editor doesn't stack extra animation loops, timers or listeners.

Installation
In Shopify admin go to Online Store → Themes → ⋯ → Edit code.
Under Sections, click Add a new section and name it interactive-brand-section.
Paste the contents of sections/interactive-brand-section.liquid and save.
In the theme editor, click Add section → Interactive brand section.
Notes
Plain Liquid, CSS and vanilla JavaScript, with no dependencies.
Fonts: the section uses your theme's heading and body fonts when available. The "Load fonts from Google Fonts" setting loads Cormorant Garamond and Inter for stores that don't provide them.
All copy is placeholder text and can be changed in the theme editor.


Author

Vidhya Prabhu: Shopify front-end developer, Goa, India.
