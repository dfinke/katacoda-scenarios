Create the `wc.ps1` PowerShell script

## Tasks

Create and set the current directory to `cli`
`md cli; cd cli`{{execute}}

Next, save the PowerShell word count script to `wc.ps1`

```
@'
param(
    [Parameter(ValueFromRemainingArguments, ValueFromPipeline)]
    $parameters
)

(Measure-Object -InputObject ($parameters -join ' ') -Word).Words
'@ > .\wc.ps1
```{{execute}}
