# IB-CEN-Responsive
Responsive template for CEN Infobytes.

#How to use
Template uses the Zurb Foundation for Emails framework, so you'll need to make sure you have that running on your computer.

See [How to install Foundation for Emails here] (https://foundation.zurb.com/emails/docs/sass-guide.html).

Once that's setup, with a new blank project loaded, copy the SRC folder from the repo into the project folder (overwrite the default folder).

Run 
	npm start

to compile the template and load the default 'index.html' page into your browser. Any file changes will be auto-reloaded.

#How to modify

Placeholder graphics are in the 'src/assets/img' folder. Replace as appropriate (update and export from the Sketch file). These graphics will be inserted sequentially. Country-specific graphics (prices etc) will be inserted automatically into the appropriate files.

Insert body item text into the grid in the 'src/partials/content.html' file. 

Update the variables at the top of 'src/pages/index.html' file. These are the lines at the top of the page between the dashes. Entr the issue number, descriptive text (to appear after the subject line when opening in email client), the path to the 'dist' folder on S3, and the subject line.

Copy the 'index.html' file and name each copy with a country code for whatever countries need to be sent a copy (AU, SG, SA, US, CA, NZ, UK & Int). Use onlt the country code for the file name (eg 'AU.html').

When you've checked everything is correct, run 
	npm run build
To compile. This will add vendor prefixes, inline all CSS and minify the HTML, as well as optimising images.

Upload the 'dist' folder to the appropriate location.