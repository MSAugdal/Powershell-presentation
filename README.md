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
er det mulig å bruke powershell for deployment og konfigurasjon av nesten </br>
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

## Basics av PowerShell bruk
Powershell bruker noe som kalles for CMDlets.
CMDlets er som ferdiglaget funksjoner som gjør en spesifikk ting,
 og tar som oftest et input, og gir et output.

cmdlets er powershell native kommandoer, altså at de stammer fra powershell, og ikke eksterne executables.

cmdlets er samlet i moduler. Du kan tenke på det som å importere er bibliotek i python, f.eks. numpy. Når du importerer en modul får du tilgang til alle kommandoene tilhørende den modulen.

cmdlets som tilhører en spesifikk modul har ofte en "preface" med navnet på modulen de stammer fra. La oss si at du importerer en AWS modul. Alle cmdlets fra AWS modulen vil da starte med AWS.

cmdlets kan bli skrevet i hvilken som helst programmeringsspråk basert på .NET. Det vil si C#, F# O.L.

PowerShell bruker et verb-substantiv navnepar for å navngi cmdlets.
 verb: get, set, create osv. substantiv: service, alias, command osv.

De viktigste CMDletene i powershell er "help", "get-command" og "get-alias".

#### get-command og get-alias
Om du er usikker på hvilken kommando du trenger, men vet at du vil hente noe, altså "get", kan du skrive "get-command get-*" eller "get-alias get-*"

"\*" er så og si universelt i alle operativsystemer, og betyr "hva som helst". "get-*" betyr da, alt som starter på "get-".

#### help command
Om du kan man pages i Linux kan du allerede help kommandoen.
Help cmdleten viser en "help page" for den spesifiserte kommandoen.
Denne help pagen som vises forklarer hva cmdleten brukes til, hva den  tar som input, hvilke CLI-flags den tar og hva den gir som output.


# Oppgaver (Oppgavene er på enkelsk, fordi det er lettere å skjønne hvilke kommandoer dere skal bruke)
1. Display a list of running processes.
2. Test the connection to google.com or bing.com without using an external command like ping.
3. Display a list of all commands that are of the cmdlet type. (Hint: Get-Command. use help to find out how to narrow down the list)
4. Display a list of all aliases.
5. Make a new alias, so you can run ntst to run netstat from a PowerShell prompt.
6. Display a list of processes that begin with the letter p. Read the help for the necessary command—and don’t forget that the asterisk (*) is a near-universal wildcard in PowerShell.
7. Make a new folder (aka directory) using the New-Item cmdlet with the name of MyFolder1. Then do it again and call it MyFolder2. Use Help if you’re not familiar with New-Item.
8. Remove the folders from step 7 in a single command. Use Get-Command to find a similar cmdlet to what we used in step 7—and don’t forget that the asterisk (*) is a near-universal wildcard in PowerShell.
