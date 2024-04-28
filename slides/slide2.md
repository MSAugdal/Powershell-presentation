## Command line shell
 
---

### Tab Completion
```ps1
PS C:\Users\Sawcon> Get-
```
<!-- .element: data-id="tab" -->

---

### Tab Completion
```ps1
PS C:\Users\Sawcon> Get-
Get-Alias                        Get-EventSubscriber              Get-ItemProperty                 Get-PSBreakpoint                 Get-Random
Get-ChildItem                    Get-ExecutionPolicy              Get-ItemPropertyValue            Get-PSCallStack                  Get-Runspace
Get-Clipboard                    Get-ExperimentalFeature          Get-Job                          Get-PSDrive                      Get-RunspaceDebug
Get-CmsMessage                   Get-FileHash                     Get-Location                     Get-PSHostProcessInfo            Get-SecureRandom
Get-Command                      Get-FormatData                   Get-MarkdownOption               Get-PSProvider                   Get-TimeZone
Get-Content                      Get-Help                         Get-Member                       Get-PSReadLineKeyHandler         Get-TraceSource
Get-Credential                   Get-History                      Get-Module                       Get-PSReadLineOption             Get-TypeData
Get-CredsFromCredentialProvider  Get-Host                         Get-Package                      Get-PSRepository                 Get-UICulture
Get-Culture                      Get-InstalledModule              Get-PackageProvider              Get-PSResource                   Get-Unique
Get-Date                         Get-InstalledPSResource          Get-PackageSource                Get-PSResourceRepository         Get-Uptime
Get-Error                        Get-InstalledScript              Get-PfxCertificate               Get-PSScriptFileInfo             Get-Variable
Get-Event                        Get-Item                         Get-Process                      Get-PSSession                    Get-Verb
```
<!-- .element: data-id="tab" -->

---

### Command prediction
```ps1
PS C:\Users\Sawcon> G
```
<!-- .element: data-id="cmd" -->

---

### Command prediction
```ps1
PS C:\Users\Sawcon> G
                    Get-command
```
<!-- .element: data-id="cmd" -->

---

### Alias
```ps1
PS C:\Users\Sawcon> ls
```

---

### Alias 
```ps1
PS C:\Users\Sawcon> Get-ChildItem
```
<!-- .element: data-id="code" -->

---

### Alias
```html
<body>
    <div>I'm a div!</div> <-- Child element of body
</body>
```
<!-- .element: data-id="code" -->

---

### Alias 
```html
<body>
    <div>I'm a div!</div> <-- Child element of body
</body>
```

```html
<Directory>
    <File>I'm a file!</File> <-- Child item of Directory
</Directory>
```

---

### Alias 
```ps1
PS C:\Users\Sawcon> Get-ChildItem
```
```console
    Directory: C:\Users\Sawcon

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         4/23/2024   6:14 PM                Homework 
f-----         4/20/2024   6:14 PM           1420 config.json
```
<!-- .element: class="fragment fade-in" data-id="console" -->

---

### Piping
```ps1
PS C:\User\Sawcon> I-Give-Output | I-Want-Input
```
<!-- .element: data-id="pipe" -->

---

### Piping
```js [1:]
const OBJECT = "I'm a string!";
```
<!-- .element: data-id="pipe" -->

---

### Piping
```js [1: 3-6]
const OBJECT = "I'm a string!";

function giveMeInput(inputStr) {
    // Do something with input
    return modifiedInput;
}
```
<!-- .element: data-id="pipe" -->

---

### Piping
```js [1: 8]
const OBJECT = "I'm a string!";

function giveMeInput(inputStr) {
    // Do something with input
    return modifiedInput;
}

console.log(giveMeInput(OBJECT));
```
<!-- .element: data-id="pipe" -->

---

### Piping
```ps1
PS C:\User\Sawcon> $OBJECT = "I'm a string!"
PS C:\User\Sawcon> $OBJECT | Out-Host
```
<!-- .element: data-id="pipe" -->
```js
const OBJECT = "I'm a string!";

function giveMeInput(inputStr) {
    // Do something with input
    return modifiedInput;
}

console.log(giveMeInput(OBJECT));
```
<!-- .element: data-id="pipe" -->

---

## Help <!-- .element: data-id="title" -->

---

## Help <!-- .element: data-id="title" -->
```ps1
PS C:\Users\Sawcon> Out-Host
```
<!-- .element: data-id="code" -->

---

## help <!-- .element: data-id="title" -->
```ps1
PS C:\users\sawcon> Out-Host
PS C:\users\sawcon> man Out-Host
```
<!-- .element: data-id="code" -->

---

## help <!-- .element: data-id="title" -->
```ps1
PS C:\users\sawcon> help Out-Host
```
<!-- .element: data-id="code" -->

---

## help <!-- .element: data-id="title" -->
```ps1
PS C:\users\sawcon> help Out-Host

NAME
    Out-Host

SYNTAX
    Out-Host [-Paging] [-InputObject <psobject>] [<CommonParameters>]

PARAMETERS
    -InputObject <psobject>

        Required?                    false
        Position?                    Named
        Accept pipeline input?       true (ByValue)
        Parameter set name           (All)
        Aliases                      None
        Dynamic?                     false
        Accept wildcard characters?  false

    -Paging

        Required?                    false
        Position?                    Named
        Accept pipeline input?       false
        Parameter set name           (All)
        Aliases                      None
        Dynamic?                     false
        Accept wildcard characters?  false

    <CommonParameters>
        This cmdlet supports the common parameters: Verbose, Debug,
        ErrorAction, ErrorVariable, WarningAction, WarningVariable,
        OutBuffer, PipelineVariable, and OutVariable. For more information, see
        about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

INPUTS
    System.Management.Automation.PSObject

OUTPUTS
    System.Object

ALIASES
    oh

REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial help.
        -- To download and install Help files for the module that includes this cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help Out-Host -Online" or
           go to https://go.microsoft.com/fwlink/?LinkID=2096863.

```
<!-- .element: data-id="code" -->

---

### Det unike med PowerShell
#### Bygget på .NET framework
```ps1
PS C:\Users\Sawcon> $String = "Hello, world!"
```
<!-- .element: class="fragment fade-in" -->

```ps1
PS C:\Users\Sawcon> $String | Get-Member

```
<!-- .element: class="fragment fade-in" -->

```ps1 [1: 1|26|39|54]
   TypeName: System.String

Name             MemberType            Definition
----             ----------            ----------
Clone            Method                System.Object Clone(), System.Object ICloneable.Clone()
CompareTo        Method                int CompareTo(System.Object value), int CompareTo(string strB), int IComparable.CompareTo(...
Contains         Method                bool Contains(string value)
CopyTo           Method                void CopyTo(int sourceIndex, char[] destination, int destinationIndex, int count)
EndsWith         Method                bool EndsWith(string value), bool EndsWith(string value, System.StringComparison compariso...
Equals           Method                bool Equals(System.Object obj), bool Equals(string value), bool Equals(string value, Syste...
GetEnumerator    Method                System.CharEnumerator GetEnumerator(), System.Collections.IEnumerator IEnumerable.GetEnume...
GetHashCode      Method                int GetHashCode()
GetType          Method                type GetType()
GetTypeCode      Method                System.TypeCode GetTypeCode(), System.TypeCode IConvertible.GetTypeCode()
IndexOf          Method                int IndexOf(char value), int IndexOf(char value, int startIndex), int IndexOf(string value...
IndexOfAny       Method                int IndexOfAny(char[] anyOf), int IndexOfAny(char[] anyOf, int startIndex), int IndexOfAny...
Insert           Method                string Insert(int startIndex, string value)
IsNormalized     Method                bool IsNormalized(), bool IsNormalized(System.Text.NormalizationForm normalizationForm)
LastIndexOf      Method                int LastIndexOf(char value), int LastIndexOf(char value, int startIndex), int LastIndexOf(...
LastIndexOfAny   Method                int LastIndexOfAny(char[] anyOf), int LastIndexOfAny(char[] anyOf, int startIndex), int La...
Normalize        Method                string Normalize(), string Normalize(System.Text.NormalizationForm normalizationForm)
PadLeft          Method                string PadLeft(int totalWidth), string PadLeft(int totalWidth, char paddingChar)
PadRight         Method                string PadRight(int totalWidth), string PadRight(int totalWidth, char paddingChar)
Remove           Method                string Remove(int startIndex, int count), string Remove(int startIndex)
Replace          Method                string Replace(char oldChar, char newChar), string Replace(string oldValue, string newValue)
Split            Method                string[] Split(Params char[] separator), string[] Split(char[] separator, int count), stri...
StartsWith       Method                bool StartsWith(string value), bool StartsWith(string value, System.StringComparison compa...
Substring        Method                string Substring(int startIndex), string Substring(int startIndex, int length)
ToBoolean        Method                bool IConvertible.ToBoolean(System.IFormatProvider provider)
ToByte           Method                byte IConvertible.ToByte(System.IFormatProvider provider)
ToChar           Method                char IConvertible.ToChar(System.IFormatProvider provider)
ToCharArray      Method                char[] ToCharArray(), char[] ToCharArray(int startIndex, int length)
ToDateTime       Method                datetime IConvertible.ToDateTime(System.IFormatProvider provider)
ToDecimal        Method                decimal IConvertible.ToDecimal(System.IFormatProvider provider)
ToDouble         Method                double IConvertible.ToDouble(System.IFormatProvider provider)
ToInt16          Method                int16 IConvertible.ToInt16(System.IFormatProvider provider)
ToInt32          Method                int IConvertible.ToInt32(System.IFormatProvider provider)
ToInt64          Method                long IConvertible.ToInt64(System.IFormatProvider provider)
ToLower          Method                string ToLower(), string ToLower(cultureinfo culture)
ToLowerInvariant Method                string ToLowerInvariant()
ToSByte          Method                sbyte IConvertible.ToSByte(System.IFormatProvider provider)
ToSingle         Method                float IConvertible.ToSingle(System.IFormatProvider provider)
ToString         Method                string ToString(), string ToString(System.IFormatProvider provider), string IConvertible.T...
ToType           Method                System.Object IConvertible.ToType(type conversionType, System.IFormatProvider provider)
ToUInt16         Method                uint16 IConvertible.ToUInt16(System.IFormatProvider provider)
ToUInt32         Method                uint32 IConvertible.ToUInt32(System.IFormatProvider provider)
ToUInt64         Method                uint64 IConvertible.ToUInt64(System.IFormatProvider provider)
ToUpper          Method                string ToUpper(), string ToUpper(cultureinfo culture)
ToUpperInvariant Method                string ToUpperInvariant()
Trim             Method                string Trim(Params char[] trimChars), string Trim()
TrimEnd          Method                string TrimEnd(Params char[] trimChars)
TrimStart        Method                string TrimStart(Params char[] trimChars)
Chars            ParameterizedProperty char Chars(int index) {get;}
Length           Property              int Length {get;}
```
<!-- .element: class="fragment fade-in" -->

---

### Scriptingspråk 
```ps1 [1:]
function Get-FolderContent() {
  get-childitem
}

Get-FolderContent
```
<!-- .element: data-id="code" -->

```ps1
PS C:\Users\Sawcon>./Get-FolderContent.ps1
```
<!-- .element: class="fragment fade-in" -->

```ps1
    Directory: C:\Users\Sawcon

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         4/23/2024   6:14 PM                Homework
```
<!-- .element: class="fragment fade-in" -->

---

### Scriptingspråk
```ps1 [1: 1-4|5|7-10|11|12]
# Functions
Function MyFunction() {
    #TODO
}
MyFunction

# Classes
Class MyClass {
    [string]$Name
}
$Obj = [MyClass]::new()
$Obj.Name = "MyName"
```

---

### Scriptingspråk
Input-output
```ps1
#    ./myscript.ps1 -Name "myname" -Age 18
param (
	[string]$Name,
	[Int32]$Age
)
Write-Output $Name
Write-Output $Age
```
<!-- .element: data-id="code" -->

---

### Scriptingspråk
Input-output
```ps1
#    ./myscript.ps1 -Name "myname" -Age 18
param (
	[string]$Name,
	[Int32]$Age
)
Write-Output $Name
Write-Output $Age
```
<!-- .element: data-id="code" -->

```ps1
PS C:\Users\Sawcon> ./myscript.ps1 -Name "MyName" -Age 18
```
<!-- .element: data-id="daddy" -->

---

### Scriptingspråk
Input-output

```ps1
PS C:\Users\Sawcon> ./myscript.ps1 -Name "MyName" -Age 18

MyName

18
```
<!-- .element: data-id="daddy" -->

