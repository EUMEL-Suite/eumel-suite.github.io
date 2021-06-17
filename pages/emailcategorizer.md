## Email Categorizer

This project is an addin for Microsoft Outlook to enrich emails.

The `EUMEL Suite Email Categorizer` is designed to add a project name to the email's subject. Project names are added to the subject with
opening and closing tags, e.g. "[" and "]" After sending an email, a dialogue is shown to select a project and see the parsed
subject. The dialogue shows the subject and the project, if a project is already set in the subject.



### Getting Started



![EUMEL Suite Categorizer](/Assets/categorizer_intro.png)

### Certificates

## Configuration

A so called outlook backstage view is added to configure the settings, storage backends and opening and closing tags. 

### Manage Categories



### Manage Settings




# Eumel Email-Categorizer

The EUMEL email categorizer is an outlook add-in to tag or categorize email in its subject. The goal is sending an email with a prefixed subject to categorize emails before it is sent.

A detailed documentation can be found in at [organization page](https://eumel-suite.github.io/pages/emailcategorizer.html).

# Basic usage

The email is written regilarily and can contain a category in brackets "[]". The subject is parsed for the category and added to the front of the subject.

![Subject Email](/Assets/categorizer_mailsource.png?raw=true)

After sending the email, a dialog is show which presents the category and the subject.

![Subject Editor](/Assets/categorizer_subjecteditor.png?raw=true)

# Configuration

The configuration is put into a "backstage view" which cna be found underneath the "File" menu.

![Configuration Entry](/Assets/categorizer_configurationoverview.png?raw=true)

The first option provides a dialog to edit the categories, which are stored during sending emails.

![Categories Editor](/Assets/categorizer_categoryeditor.png?raw=true)

The second option provides a dialog to edit the settings

![Settings Editor](/Assets/categorizer_editsettings.png?raw=true)
