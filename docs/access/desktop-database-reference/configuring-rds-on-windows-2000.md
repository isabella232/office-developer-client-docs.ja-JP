---
title: Windows 2000 に RDS を構成する
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8482df5ca2fab110e5b1a77fe227c5f0c583d893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296018"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="5bd50-102">Windows 2000 での RDS の構成</span><span class="sxs-lookup"><span data-stu-id="5bd50-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="5bd50-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bd50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5bd50-104">Windows 2000 へのアップグレード後に RDS が正しく機能しない場合は、次の手順に従って問題のトラブルシューティングを行ってください。</span><span class="sxs-lookup"><span data-stu-id="5bd50-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="5bd50-105">World Wide Web Publishing Service が最初に実行されていることを確認するために、Internet Explorer を使用して https://*サーバー*に移動します。</span><span class="sxs-lookup"><span data-stu-id="5bd50-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="5bd50-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="5bd50-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="5bd50-107">[スタート] ボタンをクリックし、[ファイル名を指定して実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bd50-107">From the Start menu, select Run.</span></span> <span data-ttu-id="5bd50-108">「msdfmap.ini」と入力して [OK] をクリックし、メモ帳で msdfmap.ini ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5bd50-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="5bd50-109">[ \[CONNECT DEFAULT\] ] セクションをチェックし、ACCESS パラメーターが NOACCESS に設定されている場合は、READONLY に変更します。</span><span class="sxs-lookup"><span data-stu-id="5bd50-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="5bd50-110">RegEdit ユーティリティを使用して、"HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\ハンドラ info" に移動し、**ハンドラ required**が0に設定されていること、および**defaulthandler**が "" になっていることを確認します (Null文字列)。</span><span class="sxs-lookup"><span data-stu-id="5bd50-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5bd50-111">[!メモ] レジストリのこのセクションを変更した場合は、コマンド プロンプトに「NET STOP W3SVC」および「NET START W3SVC」を入力して、World Wide Web Publishing Service の停止および再起動を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bd50-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="5bd50-112">RegEdit ユーティリティを使用して、レジストリ内を移動し\_、\_"\\HKEY\\LOCAL\\MACHINE\\SYSTEM\\CurrentControlSet\\service W3SVC Parameters ADCLaunch" という**キーがあるかどうかを確認します。rdsserver.datafactory。 Datafactory**</span><span class="sxs-lookup"><span data-stu-id="5bd50-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="5bd50-113">ない場合は、これを作成します。</span><span class="sxs-lookup"><span data-stu-id="5bd50-113">If not, create it.</span></span>

5.  <span data-ttu-id="5bd50-114">インターネットサービスマネージャーを使用して、既定の web サイトに移動し、MSADC 仮想ルートのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="5bd50-114">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="5bd50-115">[ディレクトリ セキュリティ] タブの [IP アドレスとドメイン名の制限] を調べます。</span><span class="sxs-lookup"><span data-stu-id="5bd50-115">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="5bd50-116">アクセスを [拒否する] が選択されている場合は、[許可する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bd50-116">If the "Access is Denied" is checked then select "Granted".</span></span>

<span data-ttu-id="5bd50-117">変更しても問題が解決されない場合は、サーバーを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="5bd50-117">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

