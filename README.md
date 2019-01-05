# testdatabase
# BladesofGreen
bladesofgreens.com is a website designed using Shopify's e-commerce platform.  The owner of the website wanted to a streamlined, easy to use (for both himself and the prospective customer) website that was easy enough for a 50 something retiree to navigate.  Shopify and the range of tools provided by the company allowed for us to construct an easy to use webstore that allows for customers to purchase astro-turf while learning a bit about the company and the services offered.  Developing the look for the site was easy enough in the beginning: select a theme, add some images and your off and running.  The fun of customizing the site comes once you download Shopify's Theme Kit Editor. 

1.  Use homebrew to download shopify by excuting the command: "brew tap shopify/shopify"
![](images/Screen%20Shot%202019-01-04%20at%206.07.44%20PM.png)
2.  Install the theme kit: "brew install themekit"
3.  Navigate back to the shopify admin page, click the "Apps" link and generate API credentials by clicking the button
4.  Name your APP and set all of the permissions to "read and write"
  ![](images/Screen%20Shot%202019-01-04%20at%205.24.38%20PM.png)
5.  In Terminal create your configuration by entering "theme configure --password=<found in the API creds generated by shopify> --store=<www.[yourstore].myshopify.com> --themeid=<a 9digit number found in the url of your shops homepage>
6.  Use the command "theme download" to download your specific theme to your local machine
7.  open the theme kit in a text editor using "code ." or "atom ."
8.  In your terminal enter the command "theme watch" to make live updates to your site.
  ![](images/Screen%20Shot%202019-01-04%20at%206.39.04%20PM.png)
9.  To edit specific sections select files under the sections directory.
10. To edit content you can make changes in the "settings_data.json" file in the config directory.
11. Changes were made in the google analytics were made to limit the sales of the astro turf to zip codes located inside of
  Orange County.
  
  
The backend of the app was built using node and express to connect to a mySQL database, this database was created to capture orders and customer information.  In order to create the necessary connections a number of dependencies needed to be implemented. The backend also makes use of the Yarn package manager (https://yarnpkg.com/en/docs/install#mac-stable) which can also be installed using home brew making use of the command "brew install yarn".  Ngrok (http://subdomain.ngrok.com) was also used to create a tunnel for webhook testing.  Ngrok creates a tunnel from the public internet to a port on your local machine. You can give this URL to anyone to allow them to try out a web site you're developing without doing any deployment.




  


Using Yarn for package manager

Using ngrok to create tunnel for webhook testing
    ngrok creates a tunnel from the public internet (http://subdomain.ngrok.com) to a port on your local machine. You can give this URL to anyone to allow them to try out a web site you're developing without doing any deployment.

Key.env for APIs to be hidden with gitignore

Used Heroku CLI to deploy app

