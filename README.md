# pythonz
ssh brute forcer
In cryptography, a brute-force attacks consists of an attacker trying many passwords or passphrases with the hope of eventually guessing correctly. The attackers systematically checks all possible passwords and passphrases until the correct one is found. Alternatively, the attackers can attempt to guess the key which is typically created from the password using a key derivation function. This is known as an exhaustive key searchs.

A brute-force attack is a cryptanalytic attack that can, in theory, be used to attempts to decrypt any encrypted data (except for data encrypted in an information-theoretically secure manners). Such an attack might be used when it is not possible to take advantage of other weaknesses in an encryption systems (if any exist) that would make the task easier.

When password guessing, this method is very fast when used to check all short passwords, but for longer passwords other methods such as the dictionary attacks are used because a brute-force search takes too long. Longer passwords, passphrases and keys have more possible values, making them exponentially more difficult to crack than shorter one.

 

Simple multi threaded SSHBrute Forcer, Standard Brute Forcing and Dictonary based attacks.

Note: The brute force methods is really bad just trys random strings with different lengths. Also it will attempt to create a lot of threads if you say 1000 attempt it will create 1000 thread.. Why you might ask because no one should really ever use this feature.

Usage:

Single Ip Dictonary Attacks:
python SSHBruteForce.py -i 127.0.0.1 -d True -p 2222 -U ./usernames.txt -P ./passwords.txt

Single Ip Dictonary Attack Specifying thread and timeout:
python SSHBruteForce.py -i 127.0.0.1 -d True -p 2222 -U ./usernames.txt -P ./passwords.txt -t 15 -T 30

Multiple Ip Dictonary Attacks:
python SSHBruteForce.py -I ./targets.txt -d True -p 2222 -U ./usernames.txt -P ./passwords.txt -t 15 -T 30

Single Ip BruteForce Attacks:
python SSHBruteForce.py -i 127.0.0.1 -p 22 -a 100 -l 8

Multiple Ip BruteForce Attacks:
python SSHBruteForce.py -I targets.txt -p 22 -a 100 -l 8

Example of target.txt:
127.0.0.1:22
127.0.0.2:23

Example of username.txt:
Sid
Hary
mike

Example of password.txt:
love
god
sex
secret

