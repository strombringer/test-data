Files generated with this PowerShell command:

```powershell
// generate file
$out = new-object byte[] 1048576; (new-object Random).NextBytes($out); [IO.File]::WriteAllBytes('.\1MB.dat', $out)

// calculate hashsum
Get-FileHash .\1MB.dat | Format-List
Get-FileHash .\1MB.dat -Algorithm SHA512 | Format-List
```

# Hashsums

| Filename | SHA256                                                           | SHA512                                                                                                                           |
| :------- | :--------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| 1MB.dat  | 9800E095F3707C01CBC8FF224157843FC6584F8EF86F73FF25A61D8233F199F2 | 6F2FEB43B1E4F348AA9D9DF7BB2A3B195D67DE2A44CF53FC713B08C6D29D93A25842E95CE50359962B4A2BC67F62622A2FD2241B433F1940EDBD6724E59365A2 |
| 5MB.dat  | 3C0E22A5BDAB1A75798BF253B7F94C336DCC423BFC001F83F5C41370039C3ED8 | 99491AF7713CC59A4CCB47C33511C8339C8481643E75AB8A8DFD604116A5DDFDCD764D1AB309E0BB53D58019D2A59C5168967960D5CE62D0F561E37618F70A79 |
| 10MB.dat | C5A9464F31556DA890E4426EE2F8CD815BC22C3D783DBE0A3FEACA02F6C5AAF3 | 57FDC19963EAE313B997257A65ADB62C3A7F334FF3DE5A0ACECC491E5387AB68F86C0573BF39F40FBB78B4740358F9093EAA1667F491AC04344EAD2F9CCB230E |