# How to hosting your Resume through GitHub Pages

## INTENDED AUDIENCE
This instruction will help computer science students who has no background with Markdown file, Jekyll, and GitHub to host their Resume through GitHub Pages.

---

## PREREQUISITES
### Getting Started
In this section, you need to prepare the items that be listed below:
1. Get yourself a Markdown editor
  * [Atom](https://atom.io) (Recommand)
  * [VSCode](https://code.visualstudio.com/)
2. Create [GitHub](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) Account
3. Download [Ruby](https://www.ruby-lang.org/en/downloads/)
4. Download [Jekyll](https://jekyllrb.com/docs/)
5. Download [Github Desktop](https://desktop.github.com/) (Optional)

---

## Instructions
**Step 1: Create a GitHub account**  
Click [here](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) will jump to Github Signup page. follow the instructions in the Signup pages you will create an account successfully.

**Step 1: Create a Repository in GitHub.**  
Once you created your GitHub Account. Login in to your GitHub Account, you will see a "**New**" button on your top left, click it.
 ![A GIF showing the step 1](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/createRepository.gif)  

 in the next page, give a name for your repository and click **create repository** button at the bottom of the page:
 ![A GIF showing the give name of repository](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/nameRepository.gif)


**Step 2: Clone the Repository.**    
On your local machine, clone the repository you just created using Atom's built-in Git functionality. Open Atom, press Ctrl+Shift+P,(On Mac OS press Command+Shift+P) and type "GitHub: Clone." Enter the URL of your repository when prompted.
 ![A GIF showing copy URL](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/copyURL.gif)
 ![A GIF showing paste URL](https://github.com/Wolfskee/EricS.github.io/blob/master/pic/pasteURL.gif)

**Step 3: Create a new Jeckyll project locally and push to your github**  
1. Once you installed the Jekyll, run `jekyll new mySite` (mySite is your project's name) to create a new Jekyll project. And then using `cd mySite` to change directory to **mySite**.
```
jekyll new mySite
cd mySite
```

2. In your mySite folder. Delete the created **index.md** file, and rename your **resume** file to **index.md** and put your new **index.md** into your mySite Project. For testing your Jekyll project, running the following code in your Command:
```
bundle exec jekyll serve
```
After enter this code in your command, you can browse your Jekyll project locaolly by visit **http://localhost:4000**

**Step 4: Choose a Jekyll Theme**  
Choose a Jekyll theme for your resume. A good place to start is the [Jekyll Themes github](https://github.com/topics/jekyll-theme). Once you've found a theme you like, follow the instruction that the theme provide and your theme setup is done. Here is an example of using **[just-the-docs](https://github.com/just-the-docs/just-the-docs)** as my theme.  

In the ```README.md```, it provides me the instruction of how to use their theme.  
![a pic shows the instruction of just-the-doc](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/picJust-the-doc.png)  
1. add the following line in ```Gemfile```:  
```
gem "just-the-docs"
```  
you need to comment the original theme and then add the new theme, the following pic shows where you need to change.  
![a pic shows gemfile](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/gemfilePic.png)  

2. add the following line in ```_config.yml```  
```
remote_theme: just-the-docs
```
![a pic shows config](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/configPic.png)  

Same for ```_config.yml``` we need to and then add the new theme.  

3. And then execute:  
```
$ bundle
```
Or install it yourself as:
```
$ gem install just-the-docs
```
4. Test it in local.
```
bundle exec jekyll serve
```
Once it works in local, we need to change few settings to let it works on GitHub Pages.  
5. In ```gemfile``` we need uncomment this:
```
gem "github-pages", "~> 228" group: :jekyll_plugins
```
which located at line 16
6. In ```_config.yml``` we need to change
```
theme: just-the-docs
```
to ```remote_theme: <repository_name_of_your_theme>```
```
remote_theme: just-the-docs/just-the-docs
```
After that, you are ready to push it to GitHub.  

**Step 5: Push Changes to GitHub**  
Once you're happy with your resume, commit your changes and push them to GitHub using following command:  
```
git remote add origin <URL_OF_YOUR_REPOSITORY>  
git branch -M main   
git push -u origin main
```
Or, you can using the Github desktop to push your code or commit your changes.
In the GitHub desktop, click the **current repository** and click **Add** and choose **Add existing repository**.
![addRepository](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/addRepository.gif)  

And then, write some update infomation in your commit information and then click commit to master, and push origin.  
![commit](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/commit.gif)  

**Step 6: Enable GitHub Pages**  
In the repository, click the settings:
![repositorySetting](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/repositoryStting.png)  

choosing **Pages**:
![page](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/choosePage.png)  


Select **Deploy from a branch** for source section and then choose the **"master"** branch and **"/(root)"** in branch section. And click **Save**.  
![branch](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/branch.png)  

Your resume should now be live at http://your-username.github.io.  
For the example you can browse https://wolfskee.github.io/


**Relating to Etter's Book**  
In Andrew Etter's book Modern Technical Writing, he emphasizes the importance of using plain text formats like Markdown to create documentation. By hosting your resume on GitHub Pages using Jekyll, you are using a plain text format that can be easily version-controlled and collaboratively edited. Additionally, by choosing a Jekyll theme for your resume, you are using a reusable and customizable template, which follows Etter's principles of efficiency and consistency.

---

## Demo
![demo](https://github.com/Wolfskee/wolfskee.github.io/blob/master/pic/demo.gif)

---

## More Resources   
[Markdown tutorial](https://www.markdowntutorial.com/)  
[Andrew Etter's book Modern Technical Writing](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)  
[Jekyll Themes](https://github.com/topics/jekyll-theme)

---

## Authors and Acknowledgments
This README was created by Eric Shu  
The website use [just-the-doc](https://github.com/just-the-docs/just-the-docs) theme

---

## FAQs
**Why is Markdown better than a word processor?**  
Markdown is a simple way of formatting text that's easy to learn and use. It's better than traditional word processors because it allows you to create documents that can be opened on any device or operating system, and because it's more efficient and allows you to focus on your content rather than formatting. Additionally, because Markdown files are plain text, they're more accessible to people with disabilities and can be easily tracked and managed using version control systems. So, if you're looking for a faster, easier, and more flexible way to create documents, Markdown might be a great choice for you!

**Why does my new Jekyll template not change on my "GitHub Page"?**  
GitHub Pages needs time for the settings to update. It would be updated in 10 mins
