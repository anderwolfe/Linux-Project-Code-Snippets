• If you want to test this locally you'll have to serve it locally using node.js. Download node from here: https://nodejs.org/en/download

• Once you have node installed you can point a terminal/cmd prompt at the folder this website is in, and do command: node server.js
    Then you'll be able to view the website at the url localhost:3000 in your web browser

• The nice thing is you don't actually need node for this to work online, we're just using node for fetch locally. Any web server will have fetch natively so you can
    just upload the pages of this like a normal static website and it will work, enabling you to use really any webhost.

• When it's time to upload this to the webhost of your choice. You'll upload everything EXCEPT: node_modules folder, package.json, package-lock.json, server.js.
    Those are the files we use locally to simulate the webhost backend, but obviously we don't need them if we're using a webhost service.

--    

• To actually modify the images/videos on this page, you just edit/add lines to the content.json file in a text editor.
    • type can be either image or youtube.
        If you wanted audio it could still just be a youtube video.

    • src can be a url, or from the images folder for an image.
        or a youtube url for a youtube video.

    • description will be the caption of the image/video that shows when you hover over it on the page.
        This is also one of the terms the search bar looks for

    • size will be the size of the thumbnail on the main page s,m,l,xl

    • showCaptions will staticly show the title and caption of a thumbnail, making it so you don't need to hover to see it.

    • alwaysShowCaptions at the top of the content.json file will broadly set all the showCaptions option, so you don't need to define it for
        each thumbnail if you don't want to.
        

◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘

Notes specifically for content.json syntax and options:

--

"thumb": "images/imagename.jpg",
You can do this if you want a thumbnail. If you don't do it, the thumbnail will just be the image. You can do this for youtube videos too.

--

"size": "s"
"size": "m"
"size": "l"
"size": "xl"
Can do these for different sized images on the main page. If left blank it will just default to medium

◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘◘