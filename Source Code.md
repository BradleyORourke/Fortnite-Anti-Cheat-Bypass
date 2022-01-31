### How to use:
```yaml
Step 1:
   Create a C# project named "FortniteLauncher"
   
Step 2:
   Copy the code below then compile.
   
Step 3:
   Copy FortniteLauncher.exe so you have two copies then rename them to "FortniteClient-Win64-Shipping_EAC.exe" and "FortniteClient-Win64-Shipping_BE.exe".
   
Step 4:
   Open Epic Games and launch Fortnite you should see a black window show you're username and Fortnite should start.
   
Step 5:
   Now you have disabled anti-cheat have some fun.
```

### Source Code
```c#
using System;
using System.Diagnostics;

public class Program
{
	public static void Main(string[] args)
	{
		string EpicUsername = string.Empty;
		
		foreach(string cmdl in args.ToString().Split(' ')) {
			if(cmdl.Contains("-epicusername=")) {
				EpicUsername = cmdl.Replace("-epicusername=", "");
				Console.WriteLine((string)"Welcome " + EpicUsername + ", Fortnite will start shortly.");
			}
		}
		
		Process.Start("FortniteClient-Win64-Shipping.exe", args.ToString());
	}
}
```
```yaml
Feel free to use this code with credit to "Bradley O'Rourke"
```
