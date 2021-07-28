# NTLMInjector
Change the password for a user using only the user's current NTLM hash and the SamSetInformationUser API

# Usage
```powershell
$domain = "MyDomain"
$username = "MyUsername"
$oldhash = "abcdabcdabcdabcdabcdabcdabcdabcd"
$newpassword = "SuperSecurePassw0rd!"
[NTLMInjector]::ChangeNTLM($null,[NTLMInjector]::GetSid($domain, $username), $oldhash, [NTLMInjector]::ComputeNTLMHash($newpassword))
```
