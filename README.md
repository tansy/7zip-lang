# 7-Zip Language Pack
A Language Pack for 7-Zip using latest version.
Only CRLF Line Ending is accepted.

# Why?
Starting in Version 24.00 Beta, the line ending was changed as Unix (LF).
The issue can be found [here](https://github.com/ip7z/7zip/issues/14).

I later on decided make Language Pack for 7-Zip with the latest version. However for some reason, many language file (e.g: fr.txt) had Unix (LF) File after 24.00 released. So, I decided convert it as CR+LF Line Ending instead (Recommended for Windows user which can use it on Windows Notepad).

# Installation
First, if you have 7-Zip is installed, You must put the following directory like this:<br/>
**C:\Program Files\7-Zip\Lang**.

However if you running in 64-bit with 7-zip 32-bit installed, put the following this:<br/>
**C:\Program Files (x86)\7-Zip\Lang**.

Once the extraction is complete, you can choose the language you want. Go to **Tools** -> **Options** and select **Language** Tab.

# English Base file (en.ttt)
The en.ttt file is simple, which this is base language file that uses **English (Default)** language. However for some reason, **en** is default language, which it should be en-US (as 0409 hex or 1033 decimal).

If you want to translate your language and new localization, Just copy en.ttt file and paste what language you want preferred. Such as Bosnian language.

## Discrepancy File Version
In most versions that came found on 7-Zip 24.05, the **en.ttt** file uses old version, indicating this:<br/>
**; 24.04 : 2024-04-05 : Igor Pavlov**

In order to update the latest version (such as 25.01), this is the example as follows:<br/>
**; 25.01 : 2025-08-03 : Igor Pavlov**

Versions below 24.04 (that uses 7-Zip 24.05 through 25.01) contains this is bug version which it came old version. We always updated new version if Igor releases 7-Zip future versions.

Also for that, the **ru.txt** file is affected, which it had 24.04.

## Where to use Text Editor?
We use Notepad2e (https://github.com/ProgerXP/Notepad2e) or Notepad++. However there is no issue at all if you want use Windows Notepad.

# Why the text is garbled if the LF Line ending like this? If I run Windows Notepad.
<img width="800" height="600" alt="LF-LineEnding-Garbled-Notepad" src="https://github.com/user-attachments/assets/71a0bb6d-5399-42c8-965a-2245c3d77107" />

This is the most common issue if you use Windows Notepad. However it does affected on Windows 2000 and Windows 10 v1803. However for some reasons, Wine (if you run Linux) Users does not affected.

**Here is the solution:**
* **For Notepad++ users:** Edit -> EOL Conversion -> Windows (CR LF)
* **For Notepad2 (including Notepad2e) users**: File -> Line Endings -> Windows (CR+LF)
* **For Mousepad users (in Linux)**: Document -> Line Ending -> DOS/Windows (CRLF)

## FeatherPad User Notice
**Applies for LXQt Desktop and Lubuntu starting in 18.10**
**SAVING THE FILE WILL SET AS UNIX (LF) LINE ENDING. THIS METHOD IS NOT RECOMMENDED!**

If some users who had installed Lubuntu (Starting in 18.10) and LXQt Desktop Environment, We strongly advise use MousePad from XFCE. If you save the file right now, the Line Ending will changed as Unix (LF).

You **MUST** use MousePad (from XFCE) so that you can use Windows (CR+LF) Line Ending.

## The Problem
LF Line Ending has several issue when you run earlier notepad (which is appeared on Windows XP), it does not affected on Wine which they applies LF Line Ending. For whatever reasons, LF Line Ending shows garbled text on notepad.

Here is the quote by Andrzej P. Wozniak (aka Usher) on Sourceforge said:
> Wrong. Use real Notepad in real Windows XP, please. Notepad honors only CRLF as EOL, separate CR or LF are ignored.

However if you run Windows 10 v1809, the Windows Notepad fixed and it supports Unix (LF) Line Ending.
