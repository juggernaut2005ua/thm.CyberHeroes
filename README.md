# thm.CyberHeroes
write-up 

briefly and clearly

first of all i started with nmap -sC -sV  , to find out info about service such as open ports and versions of servecies running on it.
<img width="1014" height="859" alt="Screenshot_20251119_154540" src="https://github.com/user-attachments/assets/01eab058-1192-4f06-94e6-34f61c3de063" />
as result nothing interesting
second step was enumerating directories on this domain
<img width="1014" height="859" alt="Screenshot_20251119_154520" src="https://github.com/user-attachments/assets/0a1139f1-b063-4190-9877-3e89cfcb7920" />
assets gave me some info about bootstrap and its version, but i didnt need it.
<img width="1014" height="259" alt="Screenshot_20251119_154615" src="https://github.com/user-attachments/assets/6021d469-5729-41cb-bff8-8275d585f581" />
next step was trying to understend logic of login,
i thouth that service uses POST request for log in
but burp made me realize that this wasn’t the case.
<img width="1014" height="859" alt="Screenshot_20251119_154134" src="https://github.com/user-attachments/assets/bd74704c-1380-46f2-b187-fd2ddd9ed10e" />
so i started to looking for same information in site code.
i found that login button realize some authenticate() function.
<img width="1920" height="884" alt="2" src="https://github.com/user-attachments/assets/6a5563c1-d98b-4ffe-9458-9a7121ca6e18" />
when i found code that provide functionality i found credentials
<img width="1919" height="881" alt="Screenshot_20251119_153036" src="https://github.com/user-attachments/assets/f69a5e8b-94cc-4230-8d26-3a90b459defa" />
and thats it 
<img width="1919" height="882" alt="4" src="https://github.com/user-attachments/assets/4aae38ab-5ea0-4197-bf98-a33daf86b429" />
