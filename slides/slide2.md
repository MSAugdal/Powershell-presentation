Command line shell 
```ps1
PS C:\User> Get-ChildItem
Homework
```
<!-- .element: data-id="code" -->



Scriptingspråk 
```ps1 [1:]
function Get-FolderContent() {
  get-childitem
}
```
<!-- .element: data-id="code" -->

```ps1
PS C:\User>./Get-FolderContent.ps1
Homework
```
<!-- .element: class="fragment fade-in" -->



Konfigurasjonsadminiastrasjon 
```ps1
PS C:\User> Set-ExecutionPolicy signed
```
<!-- .element: data-id="code" -->

Note:
This is a note
