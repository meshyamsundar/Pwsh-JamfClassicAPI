Pwsh-JamfClassicAPI
======

PowerShell Module for the Jamf Classic API

This module essentially provides a Jamf Class API focused wrapper for the `Invoke-RestMethod` cmdlet while also providing some additional functionality.  As expressly noted, this Module only supports the Classic API and not the Jamf Pro API (formatlly UAPI/Universal API).

## Goal ##

The goal currently stands to be able to provide all the funtionality of the Jamf API via a PowerShell "cmdlet."

Hopefully this will help some of the more Windows-minded Admins or even, environments where the Windows environment "rules" the Jamf environment, and so creating automated processes via other methods (python-jss) may not be an option.


## To Do ##

The following items are what are on the list to be done:

  * Improve the -Authentication method on the Invoke-JamfClassicAPI Function
  * (Much) more testing
  * Documentation, Examples, etc


## Needs to be tested ##

The following functionality has not been tested:

Invoke-JamfClassicAPI
  * Methods
    * DELETE
    * PUSH
    * PUT
    * These include using the -Body Parameter to supply the content
  * Pipeline (To/From)


## Functional ##

The following items have been tested:

Invoke-JamfClassicAPI
  * Resource Paramter "auto compelets" as desired
  * GET Method
  * Headers
    * json
    * xml
  * Verifies Method is supported by the supplied Resource
  * Data passed via the $Endpoints Parameter will successfully transpose into the requested $Resoure (so far in testing)

Get-JamfAPIResources
  * Successfully grabs all API Resources from the provided Jamf Pro Server

Set-JamfServer
  * Successfully sets the Jamf Pro Server URL

