--Readme document for Abby Pho, dppho@uci.edu--

A reminder on academic integrity, as described in the syllabus.

In general, the course staff expects that you will look at code and examples from many online resources as part of the assignments, particularly to resolve syntax and understand frameworks. We expect that you'll use other libraries you find, and will even require it in some assignments. These practices are often critical to the work of developers today. The best developers are adept at interpreting the examples they see, customizing them to their specific situation, and citing their sources so they can find them later. We expect you to do the same.

While learning from examples is encouraged, attempting to pass an existing project or example from the web as your own is not allowed. If you ever have a question about what is or is not appropriate, feel free to ask the course staff!

Talking to classmates about class material, assignment requirements, etc. is a great way to verify ideas and get feedback. But this distinctly does *not* permit attempting to pass off someone else’s code as your own. Talking over ideas and approaches is allowed, but the work that you produce and submit must be your own.

1. How many assignment points do you believe you completed (replace the *'s with your numbers)?

7.5/10
- 1/1 Readme
- 1.5/2 Basic HTML content
- 0.5/1 Basic CSS styling
- 1/1 Advanced feature
- 1.5/2 Responsive layout
- 1/1 Passes validation checks
- 1/2 Embraces spirit of the assignment

2. What (a) basic features, (b) CSS features, and (c) advanced features did you include in your portfolio?

(a) Basic features
    I created headers and footers, added images, and design the overall structure of the website.


(b) CSS features
    I used CSS to style the body, header with the ID "introduction", professional headshot image included in
    the home page's header, navigation bar, and footer.


(c) Advanced features
    Some advanced features I included in my portfolio website are:
        - Using 'd-flex', 'flex-column', and 'flex-md-row' to position the elements.
        - A navigation bar that remains at the top no matter how far you scroll down.
        - An embedded PDF of my resume and a download button (for in case the browser
          does not support embedded PDFs).



3. Did you ignore any of the warnings or errors presented by the accessibility checker? If so, why does this not seem like an accessibility concern? If it's useful, you can consolidate your thoughts on multiple warnings/errors if the rationale is similar.
    Yes, I included detailed descriptions of the cover arts (images) for the projects that I worked on and received warnings that they may be too long. But I ultimately decided to keep the descriptions because they do indeed described the images
    and I think the images are an important part of making the projects appealing to potential recruiter or any interested person, so I do not think they really fit the "decorative element" category.



4. How long, in hours, did it take you to complete this assignment?
    In total, this resume took me about two weeks to complete. With three days of designing the portfolio on Figma,
    a week and a half of deep-diving into the internet, watching tutorials, and discussing with a friend to grasp
    the basic of HTML and CSS (it is simpler than I originally fear, just a lot of shorthands that I need to remember),
    and about six days of actually coding the website (including the time I spent using an online compiler to test
    out codes).


5. What online resources did you consult when completing this assignment? (list specific URLs, describe queries to Generative AI, or use of AI-based code completion)
    These are the prompts I feed AI addressing my point of confusion, and the responses I received:
        1. How do I git commit the codes I wrote in VSCode to git?
            I'll help you commit your code to Git in VS Code. Let me first check if your workspace has Git initialized: 

            Ran terminal command: git status

            Great! Git is already initialized in your workspace. Here's how to commit your code:

            **In VS Code, use the Source Control panel:**

            1. Click the **Source Control icon** in the left sidebar (looks like a branching icon)
            2. You'll see your modified files listed under "Changes"
            3. **Stage your files:**
                - Click the **+** icon next to each file, or click **+** next to "Changes" to stage all
            4. **Write a commit message:**
                - In the message box at the top, type a descriptive message (e.g., "Add portfolio content")
            5. **Commit:**
                - Press `Ctrl+Enter` or click the **Commit** button (checkmark icon)
            6. **Push to remote (optional):**
                - Click the **...** menu and select "Push" to upload to GitHub/your remote repository

            **Or use the terminal:**
            ```powershell
            git add .
            git commit -m "Your commit message here"
            git push
            ```

            Since your working tree is currently clean, make sure you've saved your changes to the files in VS Code first. Once you modify index.html or other files, they'll appear in the Source Control panel.

        2. I created an asset folder and added my professional headshot photo to the folder, photo titled "professionalHeadshot.JPG". I wrote this line to add the image to my website: "<img src="professionalHeadshot.JPG" alt="Professional headshot of Abby Pho">", but the image is not showing up in the website. Has I wrote something wrong?
            Yes, I found the issue! The image is in your assets folder, but your `src` attribute is pointing to the root directory. You need to update the image path to include the folder:

            Change:
            ```html
            <img src="professionalHeadshot.JPG" alt="Professional headshot of Abby Pho">
            ```

            To:
            ```html
            <img src="assets/professionalHeadshot.JPG" alt="Professional headshot of Abby Pho">
            ```

            Let me fix that for you: 

            Using "Replace String in File"


            ```

            ```
            Fixed! The path now correctly points to professionalHeadshot.JPG. Your image should now display on the website.

            Made changes.
    
        3. User: Is there a way I can fixed .intro-heading::after to keep the line after text from overflowing and causing scrolling while still keeping a line that expanded the remaining space after the text?

            GitHub Copilot: Yes! The issue is that `width: 100%` on an inline-block element combined with `margin-right: 100%` is causing overflow. The best solution is to use **flexbox** to make the line fill the remaining space naturally without overflow: 

            Using "Replace String in File"


            ```

            ```
            Done! The changes:
            - **Changed `.intro-heading` to `display: flex`** - This makes it a flex container so the line can fill remaining space naturally
            - **Used `flex-grow: 1`** on the `::after` - This makes the line expand to fill available space without overflow
            - **Added `gap: 1rem`** - Replaces the margin-left for cleaner spacing
            - **Added `min-width: 0`** - Prevents the flex item from overflowing past the container

            Now the line will expand to fill remaining space after the text without causing horizontal scrolling.

            Made changes.

            User: But now on small screen, the line does not show up at all :((

            GitHub Copilot: The line is likely disappearing on small screens because the flex container is wrapping or the line is getting zero width. Let's fix this by ensuring it stays on one line and the line always gets some space: 

            Using "Replace String in File"


            ```

            ```
            Changes made:
            - **Added `flex-wrap: nowrap`** - Prevents the line from wrapping to a new line
            - **Added `overflow: hidden`** on the container - Hides any overflow while keeping content on one line
            - **Added `flex-shrink: 0`** on the line - Prevents the line from shrinking below its minimum
            - **Set `min-width: 3rem`** - Ensures the line always has a visible minimum width on small screens

            Now the line should stay visible on all screen sizes while filling the available space and not causing scrolling.

            Made changes.

            User: But I want the line to start after the end of the text. Meaning, after the word "include" and not in the middle of the text lines.

            GitHub Copilot: Using "Replace String in File"


            ```

            ```
            Done! The key change:
            - **Added `white-space: nowrap`** - Keeps all the text on a single line so the line only starts after the word "include", not in the middle
            - **Changed to `overflow-x: auto`** - Allows the line to appear after the text even on small screens; it will scroll if absolutely necessary rather than hiding the line

            Now the line will always appear immediately after "include" and expand to fill the remaining space, while keeping the text intact.

            Made changes.

            User: But I don't want the user to have to scroll to read the text. The line after the text is supposed to be a decorative element to fill the remaining empty line if the text is too long and wrap around to a second line. The line after text is there to fill up remaining space so that it looks less empty (since I already left a lot of empty space on my website).

            GitHub Copilot: Using "Replace String in File"


            ```

            ```
            Perfect! Now with `flex-wrap: wrap`:
            - The text wraps naturally on small screens
            - The line appears after the text on the same line
            - The line fills remaining space without causing scrolling
            - On small screens where there's no room, the line wraps to a new line below the text

            The `flex: 1 1 3rem` makes the line grow to fill available space while maintaining a minimum width of 3rem.

            Made changes.

            User: But now the line appears on a second line instead of the line where the text ended.

            GitHub Copilot: Using "Replace String in File"


            ```

            ```
            Changed `flex: 1 1 3rem` to `flex: 1 1 0` - this makes the line start at 0 width (so it doesn't force a wrap) and then grow to fill remaining space on the same line. The `min-width: 3rem` ensures it's always visible.

            Made changes.

            User: That doesn't help.

            GitHub Copilot: Using "Replace String in File"


            ```

            ```
            Changed to `display: inline-flex` and simplified the line to `flex: 1`. This should keep the line on the same line as the text ends instead of wrapping it to a new line.

            Made changes.

            User: That still does not help....

            GitHub Copilot: Using "Replace String in File"


            ```

            ```
            Reverted to simpler `display: flex` without wrap. This will keep the text and line on the same line without wrapping. On small screens, if space is tight, you may need to accept either: 1) Line wraps to next line (current issue), or 2) Text/line shrinks, or 3) Slight horizontal scroll on very small screens. 

            Which behavior would you prefer?

            Made changes.

            User: It's okay, can you provide comment for my current .intro-heading and .intro-heading::after explaining what the code does?

            GitHub Copilot: Read [](file:///c%3A/Users/phoph/INF133/a1-portfolio-beginnerInCodin9/styles.css#25-25), lines 25 to 45

            I see the current state is from my previous attempts. Let me check what the original was by reading the attachment provided earlier. Looking back at the original CSS provided, here are detailed comments for your current code: 

            Using "Replace String in File"


            ```

            ```
            Done! Added detailed comments explaining:
            - What `display: inline-flex` does
            - Why `flex-wrap: wrap` is used
            - How the spacing and alignment work
            - What the `::after` pseudo-element creates and how `flex: 1` makes it fill remaining space

            Made changes.
            (The entire 'Notable projects...' line is basically rewritten by AI because I couldn't figure out a way to make it work, but I ultimately gave up trying to keep the end of the text and the trailing line
            on the same line because it is more of a decorative element that would be nice to have but isn't necessary for the overall look)


6. What classmates or other individuals did you consult as part of this assignment? What did you discuss?
    I did not consult any classmates on this assignment, but I did discuss the basics of HTML and CSS with a transfer-student
    friend of mine, who has a decent knowledge of HTML and CSS. He generously explains to me the concept of specific command
    such as 'd-flex' (I was agonizing over how to put elements side by side) and rem (I was a bit confused about how it is sized).
    He also adviced me to stick with simple implementations for now and not to worry too much about the design (I spent about two 
    hours trying to figure out the navigation bar) until I have the entire website flesh out.


7. Is there anything special we need to know in order to run your code?
    No, there should not be anything special because I was trying to make everything as straight-forward as I can. In addition, this
    is not a special need, but the form on my website does not actually send a message anywhere (I asked my friend and apparently, I
    need a form service for this, but I haven't gotten to it yet).

