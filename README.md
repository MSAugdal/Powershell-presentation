# Hva er powershell?

powershell er:
- Et command-line shell
- Et scriptingspråk
- Et rammeverk for configurasjonsadministrasjon

## Powershell som command line shell
støtter populære funksjoner fra andre shell 
- Command-line history
- Tab completion
- Command prediction
- Alias (eks: ls --> Get-ChildItem)
- Piping (eks: ls | Out-File -FilePath ./out.txt)
- help system (man pages)

## Det unike med powershell shell:
- Bygget på .NET
- Støtter .NET objects som input/output

Viktigste .NET objects:
- string
- int
- float
- array
- hashmap
- custom-objects

## powershell på .NET?
Før jeg kan svare på det spørsmålet er det 1 viktig ting å vite

### Det er to versjonene av Powershell og .NET
|Powershell.exe	    |pwsh.exe		    |
|-------------------|-----------------------|
|OG powershell	    |Nye powershell	    |
|Versjon 1.0 - 5.1  |Versjon 6.0 og videre  |
|.NET framework	    |.NET Core framework    |
|Bare på windows    |Cross platform	    |
|Closed source	    |Open source	    |


## Powershell som scriptingspråk
støtte for
- classes
```ps1
Class MyClass {
    [string]$Name
    [int32]$Age = 10
    [bool]$Active = false
}
$Obj = [MyClass]::New() #initialize class
$Obj.Name = "Myname" # Access and set property
```
- functions
```ps1
Function Get-MyFunction{
    #TODO
}
Get-MyFunction # call function
```
- modules
- input output
```ps1
# lager parameterer for scriptet
# lagre koden under i en .ps1 fil og kjør den som dette:
#    ./myscript.ps1 -Name "myname" -Age 18
param (
	[string]$Name,
	[Int32]$Age
)
Write-Output $Name
Write-Output $Age
```
- Types
- Formattering av output
- Innebygget støtte for JSON, XML og CSV

## Powershell for konfigurasjonsadministrasjon
På grunn av Powershells evne til å bli utvidet med funksjoner, classes og moduler,</br>
Er det mulig å bruke powershell for deployment og konfigurasjon av nesten </br>
hvilken som helst teknologi du jobber med. </br>
F.eks:
Microsoft
- Azure
- Windows
- Exchange
- SQL

Third Pary
- AWS
- VMWare
- Google Cloud

# Oppgaver
1. Display a list of running processes.
2. Test the connection to google.com or bing.com without using an external command like ping.
3. Display a list of all commands that are of the cmdlet type. (This is tricky—we’ve shown you Get-Command, but you need to read the help to find out how to narrow down the list as we’ve asked.)
4. Display a list of all aliases.
5. Make a new alias, so you can run ntst to run netstat from a PowerShell prompt.
6. Display a list of processes that begin with the letter p. Again, read the help for the necessary command—and don’t forget that the asterisk (*) is a near-universal wildcard in PowerShell.
7. Make a new folder (aka directory) using the New-Item cmdlet with the name of MyFolder1. Then do it again and call it MyFolder2. Use Help if you’re not familiar with New-Item.
8. Remove the folders from step 7 in a single command. Use Get-Command to find a similar cmdlet to what we used in step 7—and don’t forget that the asterisk (*) is a near-universal wildcard in PowerShell.
