Prompt 1 :
I am creating a portfolio website with a hero section and a responsive grid. I want the hero section to have two columns on desktop and stack vertically on mobile. The grid should have 4 columns on desktop, 2 on tablet, and 1 on mobile. Can you provide a plan for implementing responsive breakpoints and hero behavior without giving code?

Suggestions that I accepted from Chat GPT:
1. Use flexbox for the hero section so it can stack on smaller screens.
2. Use CSS media queries to implement responsive breakpoints for desktop, tablet, and mobile.

One thing I rejected from ChatGPT and why:
ChatGPT suggested using fixed widths for all elements instead of flexible percentages or flex/minmax. 
I rejected this because fixed widths could break the layout on smaller or unusual screen sizes like tablets and mobile devices. 

Prompt 2:
On mobile screens (devices less than and equal to 600px), the hero section was not stacking vertically. The hero text and hero card remained side by side, overflowing the container and causing layout issues for those smaller layout devices
Here's the CSS part I focused on:
.hero {
  display: flex;
  padding: 20px;
}

The most important response from the AI was:
"To make the hero stack on smaller screens, you should add flex-wrap: wrap; to .hero and use a media query to set flex-direction: column; for screen widths under 600px."

Change I made to the code:
Added flex-wrap: wrap; to .hero 

Edited Code: 
@media (max-width: 600px) {
  .hero {
    flex-direction: column;
  }
}

Now the code is able to stack vertical on the smaller screens.
