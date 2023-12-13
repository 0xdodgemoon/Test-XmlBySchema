# Test-XmlBySchema
Simple PowerShell script for XML validation with XSD schema

The function Test-XmlBySchema takes two mandatory parameters: $XmlFile and $SchemaPath. These parameters are validated by the ValidateScript and ValidatePattern attributes, which ensure that the input values are existing file paths with the .xml and .xsd extensions, respectively.

To call the function Test-XmlBySchema, you need to follow these steps:

1. 
Save the function definition in a PowerShell script file, such as Test-XmlBySchema.ps1. You can use any text editor to create and edit the script file.
2. 
Open a PowerShell console or PowerShell Integrated Scripting Environment (ISE) and navigate to the folder where you saved the script file.
3. 
Dot-source the script file to load the function into the current session. Dot-sourcing is a technique that runs a script in the current scope without creating a new one. To dot-source a script, you need to use the dot operator (.) followed by a space and the path to the script file. For example:

. .\Test-XmlBySchema.ps1

1. 
Call the function by using its name and providing the values for the parameters. You can use either named or positional parameters. Named parameters use the parameter name followed by a colon and the value. Positional parameters use the value only, in the same order as the parameters are defined in the function. For example, to call the function with named parameters, you can use:

Test-XmlBySchema -XmlFile "C:\Users\user\Documents\sample.xml" -SchemaPath "C:\Users\user\Documents\schema.xsd"

To call the function with positional parameters, you can use:

Test-XmlBySchema "C:\Users\user\Documents\sample.xml" "C:\Users\user\Documents\schema.xsd"

1. 
The function will return a boolean value indicating whether the XML file is valid according to the schema file. You can assign the return value to a variable or use it in a conditional statement. For example, you can use:

$result = Test-XmlBySchema "C:\Users\user\Documents\sample.xml" "C:\Users\user\Documents\schema.xsd"
if ($result) {
Write-Host "The XML file is valid."
} else {
Write-Host "The XML file is invalid."
}
