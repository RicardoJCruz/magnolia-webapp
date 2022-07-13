# Magnolia (web-app)

#### [Visit Magnolia Live](https://magnolia123.herokuapp.com/login)

#### Video Demo:  <https://www.youtube.com/watch?v=EWgEjPe9eQ4>

#### Description: Magnolia is a web app that let's you create a profile, submit images see other people's profiles.

---

Magnolia is a simple web application made with Python, SQLite, JavaScript, HTML and CSS.

Magnolia is powered by Flask and Jinja, frameworks that use the Python language.

In Magnolia there are 3 main things you can do:

- Complete your presentation card, which is visible to anyone who visits your profile.
- Upload images and give them a title and a description to let the world know about you.
- Visit other user's profiles and discover what they are doing.

## Pages

### /register

Create a user profile in Magnolia. Go to the `/register` page and set your username and your password. Your username cannot be changed, but don't worry, as you can change your public name any time you want.

Your profile has a unique url of 11 digits. You can see your unique url along with your username in the `/settings` page.

---

### /login

Next, log in to your profile. Visit the `/login` page and enter your username and password to access your newly created profile. Once you are logged in you will be redirected to the main page `'/'`.

---

### / (dashboard)

The main page of Magnolia is your dashboard. There are 3 main elements here: your presentation card, your carousel of recent posts, and your album of uploads.

#### Presentation card

Your presentation card, at your left, will show any public information you want to share. This is the information that you can show:

- Public name,
- Profile picture,
- Company,
- Bussiness role,
- Motto,
- 3 Favorite social networks,
- Personal webpage,
- Phone number and
- E-Mail

All this information is optional, the only thing that cannot ever be empty is your public name, which by default is set to be your username. The very first time you enter your presentation card will be empty, you can make changed in the `/settings` page.

The personal webpage, the phone number, and the e-mail are rendered inside buttons. Clicking the webpage button opens a new tab that goes to that url. Clicking the phone number or the email button will copy the content to the user's clipboard.

The favorite social networks are displayed with icons, clicking them will open a new tab that goes to that url.

#### Carousel

The carousel of recent post will show the 6 more recent posts that you have made. Every post includes a picture and optional title and description.

You can cycle through the carousel's content with the arrows at each side. You can access the post that is currently show by clicking on the image or its caption (title/description), while you are hovering over this elements a white border will indicate you that clicking on them will take you to the page of this post.

If you don't have any post in your profile you will see a welcome post made by the Magnolia Team, click on it to view it.

---

#### Album

Your Album is the collection of all the posts that you have ever made. Click on one of the thumbnails to view that post.

---

### /settings

It's time to fill up your presentation card. Go to the `/settings` page by clicking on 'Your settings' found at the right side of the navbar.

In this page you can change your Profile picture. Every time you change your picture the previous one will be deleted. Remember to click the 'Change picture' button to actually make the change.

Below that, you will find your 'Public information', anything you write here will be displayed in you presentation card and it will be viewable to any person that visits your profile. The good news is that you don't need to fill any information at all, except for your public name which cannot be empty. Write, delete, and update any time you want, as much as you want. Remember to save your changes.

Do not add 'single quotes' or "double quotes" at the beginning and end of your Motto, this are displayed automatically in you presentation card.

Notice that the input fields for your 'favorite social networks' and your 'personal website' are of type `url`, this is one step of client-side validation. The text that you write here needs to follow this pattern `https://*`. If you input something that does not have that pattern at the very beginning it will be automatically added to it, so `www.something.com` will become `https://www.something.com`, this ensures that the input is accepted regardless of what the user typed.

Something else about your 'favorite social networks'... If you write a url that contains the full name of a social network  — like `https://www.instagram.com/user/` — the corresponding icon will be displayed at your presentation card in your dashboard. Otherwise, a generic globe icon is shown.

Your phone number is automatically formated as you type, a space is added every two digits for better visualization.

---

### /upload

Now that you presentation card is set up the way that you want it. You can create your first post.

Go to the `/upload` page, in the navbar click the icon of the image with a plus sign.

Once in the page you will find a form, where you can select the file that you want to upload. You can only upload images in the format of `jpg, jpeg, png`.

You can add an optional Title and Description. If you don't provide this data they will have by default "Untitled" and "No description", respectively. To prevent this write ' ' (empty space) in those fields, they will appear empty and will look better. You can edit the title of your posts once they are uploaded.

When you hit the `Upload` button you will be immediately redirected to your new post in the `/p/<post>` page.

Every post has a unique url of 11 digits. This is passed to the `/p/<post>` page to display the corresponding post.

---

### /p/\<post>

This page displays the given post with its title and description, above it shows the profile picture and the public name of the Original Poster, and below the post it displays more content uploaded by that user.

You can click on the name or image of the OP to go to their Profile Page at Magnolia.

If you are the poster of that image you will see an 'edit' button shaped like a pencil, click on it to edit the Title or the Description of your post, don't forget to apply the changes. By clicking the edit button you get access to the 'Delete image' button, which will show a confirmation modal, accept the action to entirely delete the post, you will be redirected to your dashboard.

You don't need an account to view the `/p/<post>` page.

---

### Visit other profiles

There are different ways to get to someone else's profile at magnolia.

#### url

If you have their url you can visit them without the need of an account. Something like `*/u/magnolia` will take you to Magnolia Team's Profile Page.

#### post

If you are viewing someone else's post, above the image you will find a header with the OP's profile picture and name. Click on those elements and you will get to the OP's Profile Page at Magnolia.

#### search

This may be the most convenient way of finding someone at Magnolia. In the search bar at the center of the navigation bar type a name and hit enter, this will take you to the `/search` page with the search results of that query. If you input the letter "M", the search will return any user that has that letter somewhere in their public name.

Also, you can search by url, if you input `12345678910` this will return the user who has that unique url, if any exists.

Click on a users card to visit their profile page.

...

You don't need an account to visit a user's profile page.

---

## Credits

The Welcome Post uses materials from Canvas

Photos from Unsplash by 
- Charlie Green
- Khaled Ghareeb
- Stephanie Liverani
- Quino Al
- Job Savelsberg
- Julien Riedel
- IsaaK Alexandre KaRslian
- Alek Newton
- Maxime Vandenberge
- Job Savelsberg

Some JavaScript code is inspired by examples from `w3schools`, `MDN Web Docs`, `Stackoverflow`, and `GeeksForGeeks`.

**Special thanks to CS50's staff**
