Info relating to P/Invoke and Win32 API
----
If a C/C++ method is supposed to take any sort of string parameter and write to it, trying to call that method from C# by passing a String will throw the following exception:

`Fatal error. System.AccessViolationException: Attempted to read or write protected memory. This is often an indication that other memory is corrupt.`

This is because String is immutable, so the native method cannot write to it. One possible solution is to use StringBuilder instead.

* Example code: https://stackoverflow.com/questions/10799685/how-to-pass-strings-from-c-sharp-to-c-and-from-c-to-c-using-dllimport
* Best practices for using string parameters: https://docs.microsoft.com/en-us/dotnet/standard/native-interop/best-practices#string-parameters
----
