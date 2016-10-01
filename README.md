# Windows Administrative Templates Central Store

> Repository of GPO Administrative Templates for managing Windows.


## Create Central Store

Windows uses a Central Store to store Administrative Templates files.
The ADM folder is not created in a Group Policy Object (GPO) as it is in earlier versions of Windows.
Therefore, Windows domain controllers do not store or replicate redundant copies of .adm files.


To take advantage of the benefits of `.admx` files, you must create a Central Store in the `SYSVOL` folder on a Windows domain controller.
The Central Store is a file location that is checked by the Group Policy tools.
The Group Policy tools use any `.admx` files that are in the Central Store.
The files that are in the Central Store are later replicated to all domain controllers in the domain.

To create a Central Store for `.admx` and `.adml` files, create a folder that is named **PolicyDefinitions** in the following location (for example) on the domain controller:

```
\\contoso.com\SYSVOL\contoso.com\policies\PolicyDefinitions
```

Copy all files from the `PolicyDefinitions` folder in this repository to the **PolicyDefinitions** folder on the domain controller.

[KB3087759](https://support.microsoft.com/en-us/kb/3087759)

## Administrative Templates

* Windows Server 2012 R2
* Windows 10 Version 1903
* Microsoft Office 2013
