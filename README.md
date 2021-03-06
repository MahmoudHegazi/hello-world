# Welcome to GitHub

# Upload Image On Flask Work ON Any device

PYTHON
```
# in this strange project the static folder inside templates so we added template folder statring from the main.py
UPLOAD_FOLDER = 'templates/static/uploads'
ALLOWED_EXTENSIONS = {'png', 'jpg', 'jpeg', 'gif'}

app.config['UPLOAD_FOLDER'] = UPLOAD_FOLDER

def allowed_file(filename):
    return '.' in filename and \
           filename.rsplit('.', 1)[1].lower() in ALLOWED_EXTENSIONS
           
@main.route('/image_upload', methods=['GET', 'POST'])
@login_required
def image_uploader():
    error = False
    # main_image_object.save(os.path.join(upload_path, main_image_object.filename))
    if request.method == 'POST':
        # check if the post request has the file part
        if 'main_image' not in request.files:
            flash('No file part')
            return redirect(request.url)
        file = request.files['main_image']
        # if user does not select file, browser also
        # submit an empty part without filename
        if file.filename == '':
            flash('No selected file')
            return redirect(request.url)
        if file and allowed_file(file.filename):

            x = os.path.dirname(__file__)
            upload_path = os.path.join(x, app.config['UPLOAD_FOLDER'])
            filename = secure_filename(file.filename)
            s_path = os.path.join(upload_path, filename).replace('\\', '/')
            file.save(os.path.join(
                upload_path, filename).replace('\\', '/'))

            main_image = filename
    return render_template('check.html')
    
    
```
HTML
```
 <img src="{{url_for('static',filename = 'static/uploads/download.png')}}"  style="height:280px!important;width:60%;">
```

https://developer.mozilla.org/en-US/docs/Web/API/Window/matchMedia

https://developer.paypal.com/docs/checkout/integrate/
# notify_url paypal


https://www.godaddy.com/garage/migrating-wordpress/

```
i have same problem with paypal adaptive payments in my current project. i have given my

notify_url as http://mysite.com/payment-success. In this page, i simply coded

$request = $_POST;

mail('myid@myaccount', $request);

and then i sent the transaction result to my mail to view.

Note, here in my mail i can able to see the transaction results and if i insert into database, it is inserting but i cant see the transaction results in my page. Try sending to your mail the transaction results.
```

# how to export flask
```
export FLASK_APP="flaskr"
export FLASK_ENV=development
Run the flask app

flask run
```

## important plugin
https://owlcarousel2.github.io/OwlCarousel2/demos/stagepadding.html
https://michalsnik.github.io/aos/
https://vincentgarreau.com/particles.js/
https://cssgridgarden.com/

Welcome to GitHub—where millions of developers work together on software. Ready to get started? Let’s learn how this all works by building and publishing your first GitHub Pages website!


## how to create simple framework

*  set nodejs server and add get function return json object with property and functions to make the style or animation you need
*  set js server side code extract the style and add it to some class or vairbles any one can access the object and add style
by add the client side code js in his app
## Repositories

Right now, we’re in your first GitHub **repository**. A repository is like a folder or storage space for your project. Your project's repository contains all its files such as code, documentation, images, and more. It also tracks every change that you—or your collaborators—make to each file, so you can always go back to previous versions of your project if you make any mistakes.

This repository contains three important files: The HTML code for your first website on GitHub, the CSS stylesheet that decorates your website with colors and fonts, and the **README** file. It also contains an image folder, with one image file.

## Describe your project

You are currently viewing your project's **README** file. **_README_** files are like cover pages or elevator pitches for your project. They are written in plain text or [Markdown language](https://guides.github.com/features/mastering-markdown/), and usually include a paragraph describing the project, directions on how to use it, who authored it, and more.

[Learn more about READMEs](https://help.github.com/en/articles/about-readmes)

## Your first website

**GitHub Pages** is a free and easy way to create a website using the code that lives in your GitHub repositories. You can use GitHub Pages to build a portfolio of your work, create a personal website, or share a fun project that you coded with the world. GitHub Pages is automatically enabled in this repository, but when you create new repositories in the future, the steps to launch a GitHub Pages website will be slightly different.

[Learn more about GitHub Pages](https://pages.github.com/)

## Rename this repository to publish your site

We've already set-up a GitHub Pages website for you, based on your personal username. This repository is called `hello-world`, but you'll rename it to: `username.github.io`, to match your website's URL address. If the first part of the repository doesn’t exactly match your username, it won’t work, so make sure to get it right.

Let's get started! To update this repository’s name, click the `Settings` tab on this page. This will take you to your repository’s settings page. 

![repo-settings-image](https://user-images.githubusercontent.com/18093541/63130482-99e6ad80-bf88-11e9-99a1-d3cf1660b47e.png)

Under the **Repository Name** heading, type: `username.github.io`, where username is your username on GitHub. Then click **Rename**—and that’s it. When you’re done, click your repository name or browser’s back button to return to this page.

<img width="1039" alt="rename_screenshot" src="https://user-images.githubusercontent.com/18093541/63129466-956cc580-bf85-11e9-92d8-b028dd483fa5.png">

Once you click **Rename**, your website will automatically be published at: https://your-username.github.io/. The HTML file—called `index.html`—is rendered as the home page and you'll be making changes to this file in the next step.

Congratulations! You just launched your first GitHub Pages website. It's now live to share with the entire world

## Making your first edit

When you make any change to any file in your project, you’re making a **commit**. If you fix a typo, update a filename, or edit your code, you can add it to GitHub as a commit. Your commits represent your project’s entire history—and they’re all saved in your project’s repository.

With each commit, you have the opportunity to write a **commit message**, a short, meaningful comment describing the change you’re making to a file. So you always know exactly what changed, no matter when you return to a commit.

## Practice: Customize your first GitHub website by writing HTML code

Want to edit the site you just published? Let’s practice commits by introducing yourself in your `index.html` file. Don’t worry about getting it right the first time—you can always build on your introduction later.

Let’s start with this template:

```
<p>Hello World! I’m [username]. This is my website!</p>
```

To add your introduction, copy our template and click the edit pencil icon at the top right hand corner of the `index.html` file.

<img width="997" alt="edit-this-file" src="https://user-images.githubusercontent.com/18093541/63131820-0794d880-bf8d-11e9-8b3d-c096355e9389.png">


Delete this placeholder line:

```
<p>Welcome to your first GitHub Pages website!</p>
```

Then, paste the template to line 15 and fill in the blanks.

<img width="1032" alt="edit-githuboctocat-index" src="https://user-images.githubusercontent.com/18093541/63132339-c3a2d300-bf8e-11e9-8222-59c2702f6c42.png">


When you’re done, scroll down to the `Commit changes` section near the bottom of the edit page. Add a short message explaining your change, like "Add my introduction", then click `Commit changes`.


<img width="1030" alt="add-my-username" src="https://user-images.githubusercontent.com/18093541/63131801-efbd5480-bf8c-11e9-9806-89273f027d16.png">

Once you click `Commit changes`, your changes will automatically be published on your GitHub Pages website. Refresh the page to see your new changes live in action.

:tada: You just made your first commit! :tada:

## Extra Credit: Keep on building!

Change the placeholder Octocat gif on your GitHub Pages website by [creating your own personal Octocat emoji](https://myoctocat.com/build-your-octocat/) or [choose a different Octocat gif from our logo library here](https://octodex.github.com/). Add that image to line 12 of your `index.html` file, in place of the `<img src=` link.

Want to add even more code and fun styles to your GitHub Pages website? [Follow these instructions](https://github.com/github/personal-website) to build a fully-fledged static website.

![octocat](./images/create-octocat.png)

## Everything you need to know about GitHub

Getting started is the hardest part. If there’s anything you’d like to know as you get started with GitHub, try searching [GitHub Help](https://help.github.com). Our documentation has tutorials on everything from changing your repository settings to configuring GitHub from your command line.



#  valid db insert in last project

```
    drink = Drink(title='awesome drink1', recipe='[{"color": "blue", "name":"h3mleh", "parts":3}]')
    drink.insert()

```

# alter table sql

```
ALTER TABLE `ci`.`ciuser` 
ADD COLUMN `confirm_token` VARCHAR(500) NOT NULL DEFAULT '0' AFTER `ciphoto`;
```

# store datetime in datetime db column

```
            now = datetime.now()
            date_string = now.strftime('%Y-%m-%d %H:%M:%S')
            confirmed_sent = datetime.strptime(
                date_string, '%Y-%m-%d %H:%M:%S').strftime('%Y-%m-%d %H:%M:%S')
```


# add setting page plugin

```
add_action('admin_menu', array( $this, 'addPluginAdminMenu' ), 9);    
```

https://blog.wplauncher.com/create-wordpress-plugin-settings-page/


# async

```
const zipcode = document.querySelector('#zip');
const send = document.querySelector('#demo');

const getweather = async () => {
   
    const res = await fetch('https://api.openweathermap.org/data/2.5/weather?zip=66614,us&units=metric&appid=db6608063a9d72758e29ea323da07bd1');
    
    try {
    
       const data = await res.json();
       alert(data['main']['temp']);
    
    } catch (error) {
      alert(error);
    }
}

send.addEventListener('click', getweather);

```


```
const CarModule = () => {
  let milesDriven = 0;
  let speed = 0;

  const accelerate = (amount) => {
    speed += amount;
    milesDriven += speed;
  }

  const getMilesDriven = () => milesDriven;

  // Using the "return" keyword, you can control what gets
  // exposed and what gets hidden. In this case, we expose
  // only the accelerate() and getMilesDriven() function.
  return {
    accelerate,
    getMilesDriven
  }
};

const testCarModule = CarModule();
testCarModule.accelerate(5);
testCarModule.accelerate(4);
console.log(testCarModule.getMilesDriven());

```
