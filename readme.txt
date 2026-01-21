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


6. What classmates or other individuals did you consult as part of this assignment? What did you discuss?
    I did not consult any classmates on this assignment, but I did discuss the basics of HTML and CSS with a transfer-student
    friend of mine, who has a decent knowledge of HTML and CSS. He generously explains to me the concept of specific command
    such as 'd-flex' (I was agonizing over how to put elements side by side) and rem (I was a bit confused about how it is sized).
    He also adviced me to stick with simple implementations for now and not to worry too much about the design (I spent about two 
    hours trying to figure out the navigation bar) until I have the entire website flesh out.


7. Is there anything special we need to know in order to run your code?
    No, there should not be anything special because I was trying to make everything as straight-forward as I can.

