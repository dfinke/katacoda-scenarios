This is your first step.

## Tasks

## Install the PSStringScanner module from the PowerShell Gallery

`Install-Module PSStringScanner -force`{{execute}}

## Import the PSStringScanner module

`Import-Module PSStringScanner -force`{{execute}}

## Try it out

`"123 456 789".Scan('\d+')`{{execute}}

## Create a scanner

`$scanner = New-PSStringScanner "The quick brown fox"`{{execute}}

## What can be done?

`$scanner | Get-Member`{{execute}}

## Let's Scan

`$scanner.Scan("\w+")`{{execute}}

## Once more

`$scanner.Scan("\w+")`{{execute}}

