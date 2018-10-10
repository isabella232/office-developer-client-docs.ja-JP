---
title: Windows 2000 に RDS を構成する
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1f3227e7ae60d1b656b1a7e82b4a2d41bc36844
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478521"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="6e81d-102">Windows 2000 に RDS を構成する</span><span class="sxs-lookup"><span data-stu-id="6e81d-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="6e81d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e81d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6e81d-104">Windows 2000 へのアップグレード後に RDS が正しく機能しない場合は、次の手順に従って問題のトラブルシューティングを行ってください。</span><span class="sxs-lookup"><span data-stu-id="6e81d-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="6e81d-105">World Wide Web 発行サービスが実行されている最初 Internet Explorer を使用して、https://*サーバー*に移動することを確認します。</span><span class="sxs-lookup"><span data-stu-id="6e81d-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="6e81d-106">このように web サーバーにアクセスできない場合は、コマンド プロンプトに移動し、次のコマンドでは、「NET スタート W3SVC」を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e81d-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="6e81d-107">[スタート] ボタンをクリックし、[ファイル名を指定して実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e81d-107">From the Start menu, select Run.</span></span> <span data-ttu-id="6e81d-108">「msdfmap.ini」と入力して [OK] をクリックし、メモ帳で msdfmap.ini ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="6e81d-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="6e81d-109">チェック、\[既定の接続\]セクション、およびアクセスのパラメーターは、NOACCESS に設定されている場合は読み取り専用に変更します。</span><span class="sxs-lookup"><span data-stu-id="6e81d-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="6e81d-110">RegEdit ユーティリティを使用してに移動"HKEY\_ローカル\_マシン\\ソフトウェア\\Microsoft\\DataFactory\\HandlerInfo" **HandlerRequired**が 0 に設定され、 **DefaultHandler**がかどうかを確認し、""(Null文字列) です。</span><span class="sxs-lookup"><span data-stu-id="6e81d-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="6e81d-111">[!メモ] レジストリのこのセクションを変更した場合は、コマンド プロンプトに「NET STOP W3SVC」および「NET START W3SVC」を入力して、World Wide Web Publishing Service の停止および再起動を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e81d-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span></P>



4.  <span data-ttu-id="6e81d-112">レジストリ内を移動する、レジストリ エディター ユーティリティを使用して"HKEY\_ローカル\_マシン\\システム\\CurrentControlSet\\サービス\\W3SVC\\パラメーター\\ADCLaunch] キーと呼ばれる**があることを確認し、RDSServer.Datafactory**。</span><span class="sxs-lookup"><span data-stu-id="6e81d-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="6e81d-113">ない場合は、これを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e81d-113">If not, create it.</span></span>

5.  <span data-ttu-id="6e81d-p104">インターネット サービス マネージャーを使用して既定の Web サイトに移動し、MSADC 仮想ルートのプロパティを表示します。[ディレクトリ セキュリティ] タブの [IP アドレスとドメイン名の制限] を調べます。アクセスを [拒否する] が選択されている場合は、[許可する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e81d-p104">Using Internet Services Manager, go to the Default Web Site and view the properties of the MSADC virtual root. Inspect the Directory Security/IP Address and Domain Name Restrictions. If the "Access is Denied" is checked then select "Granted".</span></span>

<span data-ttu-id="6e81d-117">変更しても問題が解決されない場合は、サーバーを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="6e81d-117">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

