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
`
Feel free to use this code with credit to "Bradley O'Rourke"
`
