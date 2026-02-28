Name: Gianni Mele
Tools used: ChatGPT, Colab, Browser

Q1: 
- Key finding (2-4 sentences): Study hours appear more predictive of exam score than sleep hours because the points more closely follow a positive trendline. Those students are closer together to the trend compared to the sleep.
- Outlier: Student A seems like an outlier because they studied only 2 hours but still scored 55, lower than expected based on the trend.

Q2:
- What was broken: Original code had the <nav> directly after <div class="logo"> but no proper spacing/flex alignment for desktop vs mobile. Grid was defined for desktop (4 columns), but no breakpoints for tablet or mobile, so it could overflow or shrink poorly.
- What I changed: Kept <header> but ensured CSS uses display: flex; justify-content: space-between. Added media queries: 2 columns for tablets (601–900px), 1 column for mobile (≤600px)

Q3:
Prompt 1 (plan, no code):
I am creating a portfolio website with a hero section and a responsive grid. I want the hero section to have two columns on desktop and stack vertically on mobile. The grid should have 4 columns on desktop, 2 on tablet, and 1 on mobile. Can you provide a plan for implementing responsive breakpoints and hero behavior without giving code?
Response snippet:
The hero section should display as two columns on desktop and stack vertically on mobile to maintain readability. The grid should adjust to 4 columns on desktop, 2 on tablet, and 1 on mobile, with flexible card widths to fit each screen size.
Accepted:
Use flexbox for the hero section so it can stack on smaller screens.
Use CSS media queries to implement responsive breakpoints for desktop, tablet, and mobile.
Rejected:
One thing I rejected from ChatGPT and why: ChatGPT suggested using fixed widths for all elements instead of flexible percentages or flex/minmax. I rejected this because fixed widths could break the layout on smaller or unusual screen sizes like tablets and mobile devices.

Prompt 2 (debug):
 On mobile screens (devices less than and equal to 600px), the hero section was not stacking vertically. The hero text and hero card remained side by side, overflowing the container and causing layout issues for those smaller layout devices
Response snippet:
To make the hero stack on smaller screens, you should add flex-wrap: wrap; to .hero and use a media query to set flex-direction: column; for screen widths under 600px.
What I verified:
- viewport sizes tested: 375px (mobile) 1200px (desktop)
- what I checked visually: whether or not the columns were stacking properly

Q4:
- Chart caption: This chart shows the relationship between students' study hours and their exam scores.
- Decision based on chart: Based on this, I would encourage students to study at least 6–8 hours for higher exam performance.
