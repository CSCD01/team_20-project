# Issue
Due to the nature of the fontproperties functionality, it replaces the current font properties with the given font properties and sets the rest of the properties as defult values. This results in inconsistant functionality as it wipes out previous changes made, such as setting the size of the text.

# Resolution
Therefore we find the solution in simply editing the text.py to ensure the proper order of operations and secure the functionality of updating the font properties. 
