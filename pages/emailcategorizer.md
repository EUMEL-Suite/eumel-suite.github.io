## Email Categorizer

This project is an addin for Microsoft Outlook to enrich emails.

[Download latest version](https://github.com/EUMEL-Suite/Eumel.EmailCategorizer/releases) in Github releases.


The `EUMEL Suite Email Categorizer` is designed to add a project name, category, or topic to an email's subject before send. Project names are added to the subject with
opening and closing tags, e.g. `[` and `]`. After sending an email, a dialogue is shown. The dialogue shows the subject and the project,
if a project is already set in the subject.

![EUMEL Suite Categorizer](/Assets/categorizer_intro.png)

After accepting the dialogue, the email is sent with the selected category in opening and closing tags. Project names or topics can
be stored for later use.

### Getting Started

After installation of this Office addin and after an email is sent, a EUMEL Categorizer dialogue pops up.

![Subject Editor](/Assets/categorizer_subjecteditor.png?raw=true)

The project can be selected from a drop down list, left ampty, or an own value can be specified. The project can
be stored for later use. By default, on forwarded and replied emails, the checkbox is unchecked.


The `Undo` button discards the parsing of the email e.g. if the opening and closing characted were not used for the project.

`Cancel` aborts the email sending process. Discarding the email must still be done in outlook. 

The `Send` button created the new subject, replaces the original one and continuous the sending process.


## Configuration

A so called outlook backstage view is added to configure the settings, e.g. storage backends and opening and closing tags.

![Configuration Entry](/Assets/categorizer_configurationoverview.png?raw=true)

The category manager allows to remove stored categories.

The settings manager allows to modify the default settings.

### Manage Categories

![Categories Editor](/Assets/categorizer_categoryeditor.png?raw=true)


The `Clear` button will clear all categories.

`Cancel` discards any changes and remains the list unchanged.

`Save` persists the list of categories

### Manage Settings

The settings editor allows the user to change the settings. 

![Settings Editor](/Assets/categorizer_editsettings.png?raw=true)

The following settings are available:

* `Category End`: closing tag
* `Category Start`: opening tag
* `List of Forward Marker`: Used to identify if an email got forwarded
* `List of Reply Marker`: Used to identify if replied to an email


* `HTTP/S URI`: Endpoint for the `Use HTTP/S source` setting
* `Storage Folder`: Storage folder for `Use JSON file` and `Use plain files`
* `Use HTTP/S source`: Load categories from http or https. This source is readonly.
* `Use JSON file`: Uses a single json file to store all settings and categories.
* `Use Outlook PST file`: Uses the outlook file to store settings.
* `Use plain files`: Uses a file per config setting. 
* `Write Storage`: Location where the categories are stored in case multiple read sources are used.


Multiple sources can be combined but categories are only stored in the `Write Storage`. The `WriteStorage` is always used as source for reading categories so it does not need to be included
in the `Use*` settings.


**Note** The registry stores the initial configuration, where to find the entire EUMEL Suite configuration settings. 

![Registry Settings](/Assets/eumel_registrysettings.png?raw=true)

`Eumel.ClearOnStart` is used to reset all changes to the default values. `Eumel.ConfigStore` is used to store the backend, where the config settings are stored. 
`Eumel.ConfigStoreSettings` are used to provide configuration settings for the config store.


### Certificates

Currently, a self signed certificate and a intermediate CA needs to be added to the certificate store.

Add [`eumel-ca.crt`](/eumel-ca.crt) to the "Trusted Root Certification Authorities"

Add [`eumel-categorizer-ca.crt`](/eumel-categorizer-ca.crt) to the "Trusted Publishers"


This will install the entire validation chain to the certificate store and trust the addin.

**BEWARE:** In case my personal root CA or intermediate CA got compromized, malicious code which is signed with the compromized certificate is trusted. This will bring your machine at a rist.

