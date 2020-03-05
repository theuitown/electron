---
layout: post
title:  "$ Create A Dark/Light Theme Switch with CSS/JS"
date:   2020-03-04 15:20:32 +0530
categories: css javascript
author: "Harsh Vardhan"
---
![Demo](https://res.cloudinary.com/practicaldev/image/fetch/s--YzRaLuxk--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://thepracticaldev.s3.amazonaws.com/i/x33qbc84dmg1yhmnnc23.gif){:height="100%" width="100%"}
<p>&nbsp;</p>
Hey, folks out there so you must have seen dark mode options in most of the websites and if you haven't seen any of it then you can take a look at my portfolio website https://iamharsh.design/ . Now if you have already done that then you are eligible to think of implementing it in your websites without a much do let's get our hand dirty with some code. Wait I have a way to do that what you have to do is just open your code in any of your favorite text editor and follow my steps.
<p>&nbsp;</p>
First thing first we will write some HTML shit to add a theme switcher button so that users can see where to click to change the theme of the website lets do it open your HTML file and add the following code into it.
<p>&nbsp;</p>
{% highlight html %}

<div class="theme-switch-wrapper">
       <label class="theme-switch" for="checkbox">
    <input type="checkbox" id="checkbox" />
    <div class="fas fa-moon moonboi fa-2x"></div>
  </label>
  </div>

{% endhighlight %}
<p>&nbsp;</p>
Here we have added a moon icon using fontawesome library its free you can use it which acts as a theme switcher its upto your choice what you wanna use inplace of moon.
<p>&nbsp;</p>
Now it might look ugly because it is only the skeleton so to make it handsome just open your CSS file and add the following code it's optional🖖(no it's not)
<p>&nbsp;</p>
{% highlight css %}


:root {
    --font-color: #424242;
    --bg-color: #fff;
}

[data-theme="dark"] {
    --font-color: #fff;
    --bg-color: #161625;
}

  .theme-switch {
    display: inline-block;
    height: 34px;
    top:2rem;
    position: relative;
    width: 60px;
  }

  .theme-switch input {
    display:none;
  }

  .moonboi{font-size: 1rem;transition: .4s;}
  .moonboi::before{transition: .4s;}

{% endhighlight %}
<p>&nbsp;</p>
Here in the above CSS shit, we have created two classes of color variables one is for light mode and one is for dark mode now after adding this what you have to do is add the variable name instead of color code wherever it is needed. Like say if you have to add color to text then you can use this like color: var(--font-color);
<p>&nbsp;</p>
So here comes the main part the implementation of theme switch based on user's choice so in order to achieve it just add the following lines into your javascript code.
<p>&nbsp;</p>
{% highlight javascript %}

const toggleSwitch = document.querySelector('.theme-switch input[type="checkbox"]');
const currentTheme = localStorage.getItem('theme');

if (currentTheme) {
    document.documentElement.setAttribute('data-theme', currentTheme);

    if (currentTheme === 'dark') {
        toggleSwitch.checked = true;
    }
}

function switchTheme(e) {
    if (e.target.checked) {
        document.documentElement.setAttribute('data-theme', 'dark');
        localStorage.setItem('theme', 'dark');
    }
    else {        document.documentElement.setAttribute('data-theme', 'light');
          localStorage.setItem('theme', 'light');
    }    
}

toggleSwitch.addEventListener('change', switchTheme, false);


{% endhighlight %}
<p>&nbsp;</p>
After merging the shitty code written above into your code you can test your website and you will see a moon icon in order to test it just click on it and you will see that theme of the whole website will change with a beautiful transition.
# Poor Man's Dark Mode
<p>&nbsp;</p>
and if you are a lazy person like me then you can just add two lines of shit into css to get dark mode
<p>&nbsp;</p>
{% highlight css %}
@media (prefers-color-scheme: light) {
	body {
              background:#fff;
	      color: #424242;
	}
}

@media (prefers-color-scheme: dark) {
	body {
		background: #161625;
                color:#fff;
	}
}
{% endhighlight %}
<p>&nbsp;</p>
Now if you are using the poor man's dark mode method then add this into css and don't give any color or background color property to any element otherwise this method will not work otherwise choice is yours 🤣.
# Back to the point
<p>&nbsp;</p>
This is pretty much it so I must take leave now if you have any issue adding it to your website you can leave a comment or if you want to have a chat with me you can DM me on Instagram at any time i have nothing to do :).
