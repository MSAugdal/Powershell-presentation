### Command line shell 
```ps1
PS C:\User> Get-ChildItem
```
<!-- .element: data-id="code" -->

---

### Command line shell
```html
<body>
    <div>I'm a div!</div> <-- Child element of body
</body>
```
<!-- .element: data-id="code" -->

---

### Command line shell 
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

### Command line shell 
```ps1
PS C:\User> Get-ChildItem
```
```console
    Directory: C:\User

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         4/23/2024   6:14 PM                Homework 
```
<!-- .element: class="fragment fade-in" data-id="console" -->

---

### Command line shell 
```console
    Directory: C:\User  <----
                            ^
Name                        |
----                        
Homework <-- Child item of Directory
```
<!-- .element: data-id="console" -->

---

#### Powershell command-line shell
- Command-line history <!-- .element: class="fragment fade-in" -->
- Tab completion <!-- .element: class="fragment fade-in" -->
- Command prediction <!-- .element: class="fragment fade-in" -->
- Alias (eks: ls --> Get-ChildItem) <!-- .element: class="fragment fade-in" -->
- Piping (eks: ls | Out-File -FilePath ./out.txt) <!-- .element: class="fragment fade-in" -->
- help system (man pages) <!-- .element: class="fragment fade-in" -->

---

### Det unike med PowerShell Shell
Støtte for .NET objects som input/output

```ps1
PS C:\User> $String = "Hello, world!"
```
<!-- .element: class="fragment fade-in" -->

```ps1
PS C:\User> $String | Get-Member

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

Scriptingspråk 
```ps1 [1:]
function Get-FolderContent() {
  get-childitem
}

Get-FolderContent
```
<!-- .element: data-id="code" -->

```ps1
PS C:\User>./Get-FolderContent.ps1
```
<!-- .element: class="fragment fade-in" -->

```ps1
    Directory: C:\User

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
MyFunction()

# Classes
Class MyClass {
    [string]$Name
}
$Obj = [MyClass]::new()
$Obj.Name = "MyName"
```

---

Konfigurasjonsadminiastrasjon 
```ps1
PS C:\User> Set-ExecutionPolicy Bypass
```
<!-- .element: data-id="code" -->
