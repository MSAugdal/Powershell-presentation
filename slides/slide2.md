Command line shell 
```ps1
PS C:\User> Get-ChildItem
```
<!-- .element: data-id="code" -->

```ps1
    Directory: C:\User

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         4/23/2024   6:14 PM                Homework
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

Konfigurasjonsadminiastrasjon 
```ps1
PS C:\User> Set-ExecutionPolicy Bypass
```
<!-- .element: data-id="code" -->
