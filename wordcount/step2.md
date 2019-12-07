Create the `wc.ps1` PowerShell script

## Tasks

Create and set the current directory to `cli`


Next, create a directory for the script and tests and save the PowerShell word count script to `wc.ps1`

```
md cli; cd cli # Create and set the directory

# Save the word count script
@'
param(
    [Parameter(ValueFromRemainingArguments, ValueFromPipeline)]
    $parameters
)

(Measure-Object -InputObject ($parameters -join ' ') -Word).Words
'@ > .\wc.ps1
```{{execute}}
