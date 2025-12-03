
Prompt Engineering Assignment — Summary Document

1. Tools Used
•	ChatGPT 
•	Vidyard for screen recording
• 	Netlify and GitHub Pages for hosting final website
•	VS Code for preview testing
•	Unsplash, Heroicons for images and icons (as needed by prompts)


2. Prompt Strategy
I created a Master Meta-Prompt that defined strict rules for:
•	Design system (spacing, typography, colors, icons)
•	Responsiveness (mobile-first, Tailwind responsive classes)
•	Code quality (semantic HTML5, clean structure, accessibility)
•	Consistency across all sections
•	Reusability across any AI tool
Then I created section-specific prompts (Navbar, Hero, Services, Contact Form, Footer) that referenced the Meta-Prompt so every component matched visually.
This allowed me to generate clean, responsive, reliable UI every time without rewriting instructions repeatedly.


3. Final Prompts Used (Master + Section Prompts)
   
A full list of the exact prompts used in the project.

===========================
MASTER META-PROMPT
===========================

You are an expert front-end developer and UI designer specializing in clean, responsive, accessible, and modern website layouts. 
Whenever I ask for a website section, follow ALL instructions below strictly:

===========================
GENERAL DESIGN RULES
===========================
1. Use **clean, semantic HTML5**.
2. Write **fully responsive Tailwind CSS classes** directly in HTML.
3. Maintain a consistent design system:
   - Rounded corners: `rounded-lg` or `rounded-xl`
   - Spacing scale: use large consistent padding (`py-16`, `px-6`) for desktop
   - Typography:
       - Headings: `text-3xl md:text-5xl font-bold`
       - Body text: `text-gray-600 text-base md:text-lg`
       - Brand/CTA: `text-indigo-600`
4. Use balanced spacing: no cramped elements.
5. All sections must look clean and modern with proper hierarchy.

===========================
RESPONSIVENESS RULES
===========================
1. Mobile-first layout.
2. Columns stack on mobile (`flex-col`, `grid-cols-1`) and expand on desktop.
3. Use `max-w-7xl mx-auto` container width.
4. Ensure images are responsive (`w-full h-auto object-cover`).

===========================
VISUAL STYLE RULES
===========================
1. Soft shadows: `shadow-md hover:shadow-lg transition`
2. Plenty of whitespace
3. Icons must be SVG (Heroicons, Feather, or Font Awesome Free).
4. Use modern, minimalist UI.

===========================
CODE QUALITY RULES
===========================
1. No inline styles.
2. No lorem ipsum — create meaningful content.
3. No broken tags or missing closing elements.
4. Clean indentation.
5. Follow accessibility best practices:
   - Buttons use `<button>`
   - Labels always connect to inputs
   - Images include `alt=""`

===========================
OUTPUT RULES
===========================
1. ALWAYS return complete working HTML.
2. Never include explanations unless I ask.
3. Never wrap code in Markdown unless I say "wrap in markdown".
4. Ensure each section can be copy–pasted independently.

Reply: “Ready for section prompts.”

===========================
SECTION-SPECIFIC PROMPTS
===========================

===========================
A. NAVBAR PROMPT
===========================
Generate a fully responsive navigation bar that follows the meta-prompt rules.

Requirements:
- Left: Brand logo text
- Right: Navigation links (Home, Services, Pricing, Contact)
- Mobile hamburger menu → opens dropdown
- Sticky top behavior (`sticky top-0 z-50`)
- Use Tailwind only
- Clean and modern look
- Use Heroicons for hamburger and close icons

Return full HTML only.

===========================
B. HERO SECTION PROMPT
===========================
Generate a premium hero section following the meta-prompt.

Requirements:
- Large heading
- Supporting description
- 1–2 CTA buttons
- Optional right-side image (Unsplash)
- 2-column layout on desktop, stacked on mobile
- Tailwind-only styling
- Clean typography and generous whitespace

Return full HTML only.

===========================
C. FEATURES SECTION PROMPT
===========================
Generate a Features section following the meta-prompt.

Requirements:
- Title + subtitle centered at top
- 3 or 6 features in a responsive grid
- Each feature includes:
  - SVG icon from Heroicons/Feather
  - Title
  - Short descriptive text
- Card-style design: rounded corners + shadow + hover effect
- Proper spacing and alignment

Return full HTML only.

===========================
D. CONTACT PROMPT
===========================
Generate a responsive Contact section that follows the meta-prompt.

Requirements:
- Title + short descriptive text
- Centered form in a rounded card with shadow
- Input fields:
  - Full Name
  - Email
  - Phone (optional)
  - Message (textarea)
- Proper label-for association
- Responsive layout
- Button with hover effects
- Include basic validation attributes: required, type="email", etc.

Return full HTML only.

===========================
E. FOOTER PROMPT
===========================
Generate a clean, modern footer following the meta-prompt.

Requirements:
- 3–4 columns on desktop, stacked on mobile
- Include:
  - Logo/brand
  - Navigation links
  - Social icon buttons (Feather Icons/Font Awesome Free)
  - Contact email
- Bottom copyright bar

Return full HTML only.

===========================
FINAL PAGE MERGE PROMPT
===========================
Combine all previously generated components (navbar, hero, services, contact form, footer) into one single HTML page.

Requirements:
- Include a `<head>` with Tailwind CDN
- Apply consistent spacing between sections
- Ensure all components are visually unified
- Do not modify any section’s design unless necessary for layout
- Return the complete working HTML page ONLY


4. Why I Wrote the Prompts This Way
Clarity & Structure
The prompts were long and extremely specific so the AI had no ambiguity about spacing, styling, responsiveness, or accessibility.
Reusability
The Master Meta-Prompt can be reused indefinitely for any front-end UI section.
It acts like a design system + coding standard combined.
Consistency
By centralizing styling rules (padding, shadows, fonts), every generated section automatically looked unified.
Reliability
The more detailed the constraints, the more consistently the AI outputs high-quality, bug-free code.


5. How I Refined the Prompts
During generation:
•	I checked responsiveness in Chrome DevTools
•	Adjusted spacing rules to avoid cramped layouts
•	Improved typography scale for mobile and desktop
•	Added accessibility requirements (labels, alt text, button semantics)
•	Ensured sections follow the same visual rhythm
•	Fixed any inconsistencies by clarifying rules in the Meta-Prompt
Every iteration made the Meta-Prompt stronger and more reusable.


6. Challenges Faced
1. Consistent Spacing Across Sections
AI sometimes outputs uneven padding.
→ Fixed by specifying exact spacing (py-16, px-6, max-w-7xl mx-auto).
2. Icon & Image Rendering Differences
Not all AI tools use the same SVG format.
→ Restricted icon sets to Heroicons/Feather for consistency.
3. Responsive Grid Behavior
Some tools generate fixed-width columns.
→ Forced mobile-first rules + Tailwind responsive classes.
4. Avoiding Inline Styles
AI occasionally uses inline CSS.
→ Clarified strict "no inline styles" rule.


7. Final Deliverables
1. Vidyard Recording Link

2. Hosted Live Website Link Netlify and Github

3. Summary Document

   

8. Conclusion
This assignment demonstrated:
•	How structured prompt engineering leads to consistent, professional UI
•	The importance of reusability, modular prompts, and a master design system
•	How iteration and refinement improve AI-generated front-end code quality
The final output is a clean, responsive, modern webpage built entirely from AI-generated code with no manual styling edits.
