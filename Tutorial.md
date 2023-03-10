# Lab Report 1

**Step 1: Installing VS Code**

Visit this link (https://code.visualstudio.com) and choose the platform that you are on (Mac, Linux, Windows)

After it is successfully installed, you should be able to open VS code and see something like this:
<img width="374" alt="image" src="https://user-images.githubusercontent.com/114766051/212496170-1018ee1e-7bf8-451f-ae85-a659b039f7cf.png">

Congrats, you've installed VS Code!

---

**Step 2: Connecting**

---

Visit this link (https://gitforwindows.org/) to install Git Bash for Windows. Once it's installed, we have to set it as the default terminal in VS Code.
1. Open the Terminal (Ctrl + ')
2. Open the command palette (Ctrl + Shift + P)
3. Type "Select Default Profile"
4. Select "Git Bash" 
5. Click on the + icon directly to the right of the terminal.
<img width="114" alt="image" src="https://user-images.githubusercontent.com/114766051/212497086-c3d206bf-7414-45e8-a486-3dd236b80b9b.png">

Now that Git Bash is your default terminal, let's connect to the remote server. To do this, visit https://sdacs.ucsd.edu/~icc/index.php. Log into your UCSD account by inputting your username and Student ID. Once you're logged in, you should see this page.

<img width="524" alt="image" src="https://user-images.githubusercontent.com/114766051/212503350-80a61de3-c8cf-4fd2-8599-13826c2ff1b4.png">

Write down the three letters that are boxed in the picture (your letters are different). Then click on the boxed link.
Now, click the link that says "change your password". Enter your current and new passwords, and when finished, DON'T click the check your password button. Instead, simply click return/enter on your keyboard when your cursor is selecting the confirm password field.

<img width="355" alt="image" src="https://user-images.githubusercontent.com/114766051/212503494-5b0d5acb-cd22-464b-8e99-80da4f6dd299.png">

Great, your password is changed!

---

Now, open VS code and open the terminal. Type in $ ssh cs15lwi23zz@ieng6.ucsd.edu, but replace "zz" with the three letters that you wrote down earlier. When the terminal asks about the authenticity of the host and if you want to continue, type yes and hit enter. Then, type in your password when prompted. It may take 15-60 minutes from when you changed your password for it to work, but when it does, you should see this.

<img width="538" alt="image" src="https://user-images.githubusercontent.com/114766051/212504041-395334e7-f695-4309-b53d-5c69318d51ad.png">

Great, you're now remotely connected!

---

**Step 3: Running Commands**

---

Now that you've connected, try running some commands, like cd, ls, cat, mkdir, pwd, and exit.

<img width="747" alt="image" src="https://user-images.githubusercontent.com/114766051/212504509-bf20fe8e-336c-4e56-97cb-89c3ade89bb7.png">

And you're all set! Thanks for reading my tutorial!
