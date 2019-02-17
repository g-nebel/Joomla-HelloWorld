# Joomla-HelloWorld Component using Github for Update Server

This example component is based on Joomla-HelloWorld from
the Tutorial Developing an MVC Component
https://docs.joomla.org/J3.x:Developing_an_MVC_Component

The component uses Github for update server.
Update links lead to the component github repository.
No extra script is needed.
After every release commit the commit is tagged with the version nummber of the release. 
By this way the release gets a release on Github and a link to zip and tar.gz of the repository

The repository contains extra files
- **com_helloworld.xml** Extension update server manifest (single extension's manifest)
- **release.txt** Release info of the current release

see:
https://docs.joomla.org/Deploying_an_Update_Server

##com_helloworld.xml
Contains all updates.

For every new release a  _\<update\>_ section for the release must be added.
In these links are changed

\<infourl title="Hello World"\>https://raw.githubusercontent.com/g-nebel/Joomla-HelloWorld/**_{current release tag}_**/release.txt\</infourl\>

\<downloadurl type="full" format="zip"\>https://github.com/g-nebel/Joomla-HelloWorld/archive/**_{current release tag}_**.zip\</downloadurl\>

The link to this file in the extension manifest uses the current file of the branch (e.g. _update-server_ ) so it will fetch the newest version of this file.

##release.txt
I used a text file in user examples a html file is used.
The old release.txt is replaced by the release.txt of the current release