# Powershell for Developers

Ppowershell
https://github.com/brentestewart/PowerShellTalk
Get-Help example
Get-Help Select-Object

Get-ChildITem
Get-ChildItem Directory
Get-ChildItem File

dir | Get-Member

dir | Out-GridView –PassThru | Set-Content

Set-Alies np notepad.exe
$dev = “c:\development”
$pets = @(“dog”, “cat”)
$pets = “snake”, “gorilla”, “dog”
$myPets = @{dog=”Beans”; cat=”cooper”;}

Comparisons us –eq, -gt, etc
Where-Object (alias wherew)
Select-Object Ialias select)
Sort-Object (alias sort)
for ($i=0; $i –lt 2; $i++) {echo $i;}
dir *.txt | foreach {$_.name, $_.length}

Powershell Providers
Get-PsProvider
cd Cert:
There are SQL Server providerds and others
https://msdn.microsoft.com/en-us/library/ee126186(v=vs.85).aspx

Functions
function add($x, $y)
{
$x +$y
}
add 2 3

Writing a Cmdlet in C#
There’s no built-in powershell, we need to do something.
NuGet: Microsoft.Powershell.5.ReferenceAssemblies
public class UpdatePhotoCmdlet : Cmdlet {
  [Paramater(ValueFromPipelineByPropertyName = true, ValueFromPipeline=true]
  public FileInfo Photo {set; get;}
  protected override void processRecord()
  {
    base.ProcessRecord();
  if (Photo?.Extension!=”.jpg”) return;
   var createDate = default(string);
  using (FileStream fs = new FileStream(Phot.FullName, FileMode.Open, FileAccess.Read)
    {
      var image = Bitmap.Create(fs);
      var metadata = (BitmapMetadata)image.Metadata;
      createDate = metadata.DateTaken;
    }  
    Photo.CreateTime = DateTime.Parse(createonDate);
    WriteObject(Photo);
  }
}
Now at Powershell, bring the module in:
Import-Module ‘C:\bin\ps\src\UpdatePhotoCmdlet\bin\UpdatePhotoCmdlet.dll’\
cd .\photos
dir | Update-Photo | sortPhotos –RootPath c:\photos


Profiles
There are  6 profiles:
Current User: $Home\Documents\WindowsPowerShell\profile.ps1
All Users: $PsHome\Microsoft.Powershell_profile.ps1
Host: …

Powershell.org

