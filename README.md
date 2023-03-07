# How to hosting your Resume through GitHub Pages

## INTENDED AUDIENCE
This instruction will help computer science students who has no background with Markdown file, Jekyll, and GitHub to host their Resume through GitHub Pages.

## PREREQUISITES
### Getting Started
In this section, you need to prepare the items that be listed below:
1. Get yourself a Markdown editor
  * [Atom](https://atom.io)
  * [VSCode](https://code.visualstudio.com/)
2. Create [GitHub](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) Account
3. Download [Ruby](https://www.ruby-lang.org/en/downloads/)
4. Download [Jekyll](https://jekyllrb.com/docs/)

## Instructions
**Step 1**: Create a Repository in GitHub.  
Once you created your GitHub Account. Login in to your GitHub Account, you will see a "**New**" button on your top Left.
 ![A GIF showing the step 1](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/createRepository.gif)  
 give a name for your repository:
 ![A GIF showing the give name of repository](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/nameRepository.gif)

**Step 2**: Choosing a Jekyll Theme for Your GitHub Page.  
Go the the SETTINGS section of your repository. In the SETTINGS section, there will be a GitHub Pages section. In this section, there is a button "**Theme Chooser**" to select your a Jekyll Theme. This will redirect you to a page where you select and preview a handful of themes. Choose the one that you like best.
![A GIF showing how to choose theme]()



**Step 3**: Clone the Repository.  
On your local machine, clone the repository you just created using Atom's built-in Git functionality. Open Atom, press Ctrl+Shift+P,(On Mac OS press Command+Shift+P) and type "GitHub: Clone." Enter the URL of your repository when prompted.
 ![A GIF showing copy URL](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/copyURL.gif)
 ![A GIF showing paste URL](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/pasteURL.gif)

**Step 4: Hosting in GitHub Pages.**  
1. Once you installed the Jekyll, run `jekyll new mySite` (mySite is your project's name) to create a new Jekyll project. And then using `cd mySite` to change directory to **mySite**.
![A pic showing jekyll new mySite](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/jekyllNew.jpg)
![A pic showing cd mySite](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/cdMysite.jpg)

2. Delete the created **index.md** file in your mySite project, and rename your **resume** file to **index.md** and put your new **index.md** into your mySite Project.

3. Push your mySite project into your GitHub. Using code:  
```
git remote add origin <URL_OF_YOUR_REPOSITORY>  
git branch -M main   
git push -u origin main
```

Step 5: Choose a Jekyll Theme
Choose a Jekyll theme for your resume. A good place to start is the Jekyll Themes website. Once you've found a theme you like, copy the files for that theme into your repository. Make sure to include any dependencies or assets that the theme requires.

Step 6: Customize the Theme
Customize the theme to your liking. This may involve modifying the theme's configuration file, adding custom CSS, or changing the layout of the resume.

Step 7: Preview Your Resume
To preview your resume locally, open a terminal in VS Code and run the command "bundle exec jekyll serve". This will start a local Jekyll server, which you can view in your browser at http://localhost:4000.

Step 8: Push Changes to GitHub
Once you're happy with your resume, commit your changes and push them to GitHub using VS Code's Git functionality.

Step 9: Enable GitHub Pages
In the repository settings on GitHub, enable GitHub Pages and choose the "main" branch as the source. Your resume should now be live at http://your-username.github.io.

Relating to Etter's Book
In Andrew Etter's book Modern Technical Writing, he emphasizes the importance of using plain text formats like Markdown to create documentation. By hosting your resume on GitHub Pages using Jekyll, you are using a plain text format that can be easily version-controlled and collaboratively edited. Additionally, by choosing a Jekyll theme for your resume, you are using a reusable and customizable template, which follows Etter's principles of efficiency and consistency.

Demo

More Resources
Markdown tutorial
Andrew Etter's book Modern Technical Writing
Jekyll Themes
Authors and Acknowledgments
This README was created by the OpenAI GPT-3 language model with contributions from the OpenAI team.

FAQs
Why is Markdown better than a word processor?
Markdown is better than a word
