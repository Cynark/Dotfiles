# Dotfiles
i3 Forest Customization config files

![i3 Forest](https://user-images.githubusercontent.com/109734366/180436048-dd60aea4-4652-464f-90ed-53f214e27121.gif)

You can see the full project created on YouTube!

Link: Soon


# Walkthrough

I'm gonna show you exactly how you can achive this look step by step.

You can also watch the tutorial I made on Youtube : Soon 

In this process we're going to use:
- i3
- Git
- Feh
- Rofi
- Vim
- i3-gaps
- Cmatrix
- Compton

# i3

Let's begin from the start, I assume you've just installed ubuntu :point_down:

![image](https://user-images.githubusercontent.com/109734366/180432457-8231908c-6429-4277-836c-55ae02850c1b.png)

Now open up the terminal and type :keyboard:: 

```sudo apt update && sudo apt upgrade```

Then

```sudo apt install i3```

Nice now you have the windows manager i3 installed :ok_hand:

Wait before continuing, what exactly is a window manager? 

**_A window manager is system software that controls the placement and appearance of windows within a windowing system in a graphical user interface._**

Great now you know what a window manager is. :bulb:

Now log out of your desktop 

![image](https://user-images.githubusercontent.com/109734366/180414412-7f44673e-224f-4cba-a5cb-b788caf42ac0.png)

Choose the account you want to log in with but now instead of typing your password and logging in, pay attention to that cog icon on the right-bottom corner.

![image](https://user-images.githubusercontent.com/109734366/180415792-65b1da20-e12c-4e42-b252-8a62af27694c.png)

Click on it and you should see four options, click on i3, type out your password and press enter.

Now you'll see this screen :desktop_computer:: 
![image](https://user-images.githubusercontent.com/109734366/180420957-d1e8fc01-5a0c-431b-be14-520ebd0b8b0a.png)


Press Enter.


Now you have to choose your mod key between WIN & ALT. Mod key is the key you use to work with i3. Opening terminals, Movements of the terminals, , custom keybindings, all depend on your mod key, so make sure your comfortable with the one you choose. (You can choose one by first pressing the key and then enter)

![image](https://user-images.githubusercontent.com/109734366/180421002-a1bb61d0-4351-4e4f-8af3-453d27b6298d.png)


Tip: you can open up a terminal by holding the mod key and pressing the return / enter key.
Terminal: Mod + Enter

You can learn more about i3 keybindings and movement keys in: https://i3wm.org/docs/userguide.html

Now your good to go! :clap:

# Git

Before installing any other tool, let's make sure we have our git installed so we're not gonna run into any errors.

In the terminal run:
```sudo apt install git```

Perfect! :dizzy:

Documentation: https://git-scm.com/doc

# Vim

Also if you want to be able to edit any config file, you obviously need a text editor. Vim is one of the most famous choices, but you could also do the same with nano, mousepad, VScode, or any other text editor that you prefer.

So again simply run:
```sudo apt install vim```

And now we have our text editor, Nice job!

Documentation: https://www.vim.org/docs.php

# Terminal Customization

It's time to start our customization. I like to start with the terminal, since it's the first thing you encouter and the main thing you would use most of the time. 

Open up the terminal menu and click on preference.
![image](https://user-images.githubusercontent.com/109734366/180425382-58fbabd4-bd3e-4ad2-bd0c-1ead61142592.png)

On the left side bar click on Unnamed section and you'll be able to see 5 tabs that you can customize: Text, Colors, Scrolling, Command, Compatibility

For now we're gonna only make 3 changes.

1. Text Font
Check the Custom font checkbox and start customzing the font. I like to change it to Noto Mono 24. Of course change it to whatever suits you best.

2. Colors
In the colors tab Uncheck the "transperency from system" theme and check "use transparent background". Drag the circle to the right so the transparency is full. Now you shouldn't see any diffrence (Only the color is going to change to black), but later on when we install compton, the change will take effect. Next I would change the Pallette so my terminal has the colors that I like the most.
This is my Pallete
![image](https://user-images.githubusercontent.com/109734366/180426518-a77c9f94-5848-4d57-8264-339d2d2ceb83.png)

Red: #C01C28
Gray: #727472
Blue: #2A7BDE
Brown: #A2734C
Green: #2AA198
Black: #545050
Orange: #F66151
Purple: #A347BA
Dark gray: #545050
Light Gray: #D0CFCC
Light Purple: #C061CB

3. Scrolling
On the Scrolling tab uncheck Show scrollbar. If your mouse wheel isn't broken you wouldn't use it as much.

Now our setting is set, we still have some more customizations to do with the terminal. You'll see them in the i3-gaps & Compton section.

# Feh
The base of your customization is your desktop wallpaper. Everything should be synchronized with the wallpaper you choose, so be careful when picking one. Now to change our wallpaper first we need to install feh. Feh is a light-weight, configurable and versatile image viewer.

To install: 
```sudo apt install feh```

Next you need to find and download your wallpaper. Feel free to use the wallpaper I found and used.

![image](https://user-images.githubusercontent.com/109734366/180428108-3cb4642c-ed8f-4988-9266-705c29248501.png)

Link: https://www.pexels.com/photo/green-leaves-1072179/

Now you have your wallpaper downloaded in the Downloads directory. I like to move it to the Pictures directory since it's more relevant to the file we have.

Run: 
```
cd Downloads
mv wallpaper.jpg ~/Pictures
```
Good, now you have your wallpaper in the Pictures directory. :camera:

To make this wallpaper permanent on your desktop you need to change the config file of the i3.

Navigate to the config file and open it up with vim:
```
cd .config
cd i3
vim config
```

Go to the bottom of the page by pressing Shift+g and press i to enter insert mode.

Now add:
```
exec_always --no-startup-id feh --bg-fill ~/Pictures/wallpaper.jpg
```

Press Esc key then type: :wq

Your file is saved. Press Alt+Shift+e to logout of i3. There will be a orange message on the top of the screen, just click on Yes, exit i3.

Now log in again. And you should see your wallpaper ready. Congrats. :tada:

# i3 Bar
There are many ways that you can customize the bar in i3. The most famous one is polybar. But since I don't like to have any bar at all I like to hide the i3 bar and have a clean screen.

Open the i3 config file again, scroll down until you can see the bar section.
Add these two lines:
```
hidden_state hide
mode hide
```
![image](https://user-images.githubusercontent.com/109734366/180431541-5602a924-34c6-4b33-942a-2e0c753e46d5.png)

And the annoying bar is out of the way, Great!. :confetti_ball:

# Cmatrix
If you're an Ethical Hacker or just a fan of hacking movies this feature here is one that you would like the most. 

Open up the terminal and run the command:
```sudo apt install cmatrix```

Now run : ```cmatrix```

Now this matrix-like terminal will make you feel more like a hacker.
![image](https://user-images.githubusercontent.com/109734366/180427538-60e8bdce-f7b3-4561-bf56-d9b162a1fdba.png)

# Compton
To activate the transparency of the terminals you need to install compton.

Command:
```sudo apt install compton```

Navigate to the config file and open it up with vim:
```
cd .config
cd i3
vim config
```
Go to the buttom of the page by pressing Shift+g and press i to enter insert mode.

Add: 
```
exec_always --no-startup-id compton compton
```

save the file by pressing Esc and typing :wq.

Press Alt+Shift+r to refresh i3 and you'll have a nice looking transparent terminal in front of you.
![image](https://user-images.githubusercontent.com/109734366/180430037-48ba1726-9000-4fdc-8300-3e4f8fd495a9.png)

# i3-gaps
I like to have some gaps between my terminals and the way to that is by i3-gaps.

To install: 
```
sudo apt install libxcb1-dev libxcb-keysyms1-dev libpango1.0-dev libxcb-util0-dev libxcb-icccm4-dev libyajl-dev libstartup-notification0-dev libxcb-randr0-dev libev-dev libxcb-cursor-dev libxcb-xinerama0-dev libxcb-xkb-dev libxkbcommon-dev libxkbcommon-x11-dev autoconf xutils-dev libtool automake
mkdir /tmp/build 
cd /tmp/build
git clone https://www.github.com/Airblader/i3 i3-gaps
cd i3-gaps
git checkout gaps && git pull
sudo apt install meson asciidoc
meson -Ddocs=true -Dmans=true ../build
meson compile -C ../build
sudo meson install -C ../build
```

And you should be good.

Now Navigate to the config file and open it up with vim:
```
cd .config
cd i3
vim config
```

Go to the buttom of the page by pressing Shift+g and press i to enter insert mode.

Add these three lines: 
```
for_window [class=".*"] border pixel 0   
                        gaps inner 15                            
                        gaps outer 15
```

The first line will make the borders of the terminals disapear and the other two lines are the gaps that will make spaces between terminals.


# And...
There are three more things that I didn't cover since they need a lot of explanations. Those include:
- Rofi
- Layouts
- Vim plugins

So to make the explanation easier I made YouTube tutorials for all of them!

YouTube Videos: Soon

# The Final word

When I first encountered the idea of customizing Linux, I didn't have enough knowledge and resources to start. I would watch other people being proud of what they had created and feel stupid.

You can see these masterpieces youself: https://www.reddit.com/r/unixporn/

But one time I decided to do whatever it takes to make my own customized machine. It took me 4 days or more specifically 8 hours to research, find, create, and customize.

I made this tutorial for those who are like my old self and are willing to start but don't know exacly how.

I hope this actually hepled you to get a idea of how actually these things are customized.

Thank you for reading!
