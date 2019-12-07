Create the wc.tests.ps1 PowerShell script

## Tasks

Save the PowerShell word count test script to `wc.tests.ps1`

```
@'
Describe "Count test" {
    It "Should equal 4" {
        $actual = .\wc.ps1 a b c d
        $actual | Should Be 4
    }

    It "Should equal 3 from piping" {
        $actual = 'a b c' | .\wc.ps1
        $actual | Should Be 3
    }
}
'@ > .\wc.tests.ps1
```{{execute}}
