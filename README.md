im too lazy to update this so it'll be archived soon
我太懶了所以我可能會放棄繼續更新中文化

# VRCX

[![GitHub Workflow Status](https://github.com/kamiya10/VRCX/actions/workflows/github_actions.yml/badge.svg)](https://github.com/kamiya10/VRCX/actions/workflows/github_actions.yml)
[![VRCX Discord Invite](https://img.shields.io/discord/854071236363550763?color=%237289DA&logo=discord&logoColor=white)](https://vrcx.pypy.moe/discord)

[原文](https://github.com/pypy-vrc/VRCX/blob/master/README.md)

VRCX 是一個提供好友管理的輔助應用程式。這個程式使用非官方的 VRChat API (VRCSDK)。

pypy & Natsumi 將不對使用 VRCX 引起的任何問題負責。***使用時請自負風險！***


## How to install VRCX

* Download latest release setup from [here](https://github.com/pypy-vrc/VRCX/releases/latest).
* Run `VRCX_Setup.exe`.

## Is VRCX against VRChat ToS?

**TL;DR:** no, as long as you don't use the Steam account login method.

*VRChat 官方對於 API 使用的立場列在它們 Discord 伺服器中的 #faq 頻道中。*
![vrchat api](https://user-images.githubusercontent.com/11171153/114227156-b559c400-99c8-11eb-9df6-ee6615b8118e.png)

### 關於 VRChatRPC.DLL

VRChatRPC.DLL 是用來以 **Steam 帳號** 登入時使用的。（如果您在登入畫面上按下使用 Steam 登入按鈕）

如果你不需要以 Steam 登入，VRChatRPC.DLL 則將不會使用到。

詳細來說，VRChatRPC.DLL 將會存取 VRChat 程序（DLL 注入）並呼叫 Steam API 來獲取登入權杖。這可能會導致你被 VRChat 封鎖。

在安全方面上還沒有採取任何技術（當然我不能說沒有風險，不過沒有問題），但不知道以後會發生什麼事。

畢竟你無法以一般的的方式登入到一個第三方帳號，所以這是唯一的方法。

它的源代碼在 https://github.com/pypy-vrc/VRChatRPC 。

## 螢幕截圖
![2fa](https://user-images.githubusercontent.com/25771678/63169786-a810f880-c072-11e9-9ede-0a3a03d5da12.png)
![01feed](https://user-images.githubusercontent.com/58339640/173773788-6b2593d6-06eb-47c9-acc6-33304b8409c8.png)
![02gamelog](https://user-images.githubusercontent.com/58339640/173773933-0dfb8e44-23dc-4f67-b254-e869f63bd51a.png)
![03search](https://user-images.githubusercontent.com/58339640/173774104-e3df96b9-3de9-47a9-8572-b32adf5f7ddf.png)
![09w1](https://user-images.githubusercontent.com/58339640/173774320-970e888c-5d65-4501-ba9f-d4fbeefc8cb6.png)
![09w2](https://user-images.githubusercontent.com/58339640/173774443-c974ad07-1f1c-44b5-9fa2-4599caa8024a.png)
![04fav](https://user-images.githubusercontent.com/58339640/173774763-59237db9-cd98-4caa-9c7a-0ebd86f77b25.png)
![05fr](https://user-images.githubusercontent.com/58339640/173774660-4f06afca-c9e3-4b44-9c1f-e4240e42860b.png)
![06mo](https://user-images.githubusercontent.com/58339640/173775059-8bf2bdd2-29f1-40b0-b10d-cf11b799617d.png)
![07no](https://user-images.githubusercontent.com/58339640/173775085-a66b020a-d0ec-43fe-bdcd-663633135c84.png)
![08op1](https://user-images.githubusercontent.com/58339640/173775126-487ece22-1937-4bc8-98fb-981697c5b704.png)

## 如何安裝 VRCX

* 下載最新發行版本 [zip](https://github.com/kamiya10/VRCX/releases/latest) 。
* 解壓縮壓縮檔。
* 執行 `VRCX.exe` 。

## 如何在 Linux 上執行 VRCX

* [指南](https://github.com/RinLovesYou/VRChat-Linux/wiki/VRCX) by @RinLovesYou

## 如何從原始碼建置 VRCX

* 取得原始碼
    * 下載最新的原始碼 [zip](https://github.com/pypy-vrc/VRCX/archive/master.zip) 或使用 `git clone` 直接複製 repo 。

* 建置 .NET
    * 安裝 [Visual Studio](https://visualstudio.microsoft.com/) 如果你還沒安裝的話。
    * 在 Visual Studio 中 "勘起專案/解決專案" 並選擇附在原始碼內的 [解決方案檔](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file) 。
    * 將 [專案設定](https://docs.microsoft.com/en-us/visualstudio/ide/understanding-build-configurations?view=vs-2019) 設為 `Release` ，平台設為 `x64` 。
    * 復原 [NuGet](https://docs.microsoft.com/en-us/nuget/consume-packages/package-restore#restore-packages-automatically-using-visual-studio) 套件。
    * [建置](https://docs.microsoft.com/en-us/visualstudio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio) 解決方案。

* 建置 Node.js
    * 下載並安裝 [Node.js](https://nodejs.org/en/download/) 。
    * 執行 `build-node.js.cmd` 。
    * 執行 `make-junction.cmd` 。

* 產生發行壓縮檔
    * 使用 [Bandizip](https://www.bandisoft.com/bandizip) 的話請執行 `make-zip.cmd` 或使用 [7-Zip](https://www.7-zip.org) 請執行 `make-zip-7z.cmd` 。
