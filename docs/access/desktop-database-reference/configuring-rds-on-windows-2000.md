---
title: Windows 2000 に RDS を構成する
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c69cdbaf30a2c592790942a04c777b11512631f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565773"
---
# <a name="configuring-rds-on-windows-2000"></a>Windows 2000 での RDS の構成


**適用先:** Access 2013、Office 2013

Windows 2000 へのアップグレード後に RDS が正しく機能しない場合は、次の手順に従って問題のトラブルシューティングを行ってください。

1.  ワールドワイド Web 発行サービスが最初に実行されているのを確認するには、次の https://*を* 使用Internet Explorer。 If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".

2.  [スタート] ボタンをクリックし、[ファイル名を指定して実行] をクリックします。 「msdfmap.ini」と入力して [OK] をクリックし、メモ帳で msdfmap.ini ファイルを開きます。 [既定の接続] セクションを確認し、ACCESS パラメーターが NOACCESS に設定されている場合は、 \[ \] それを READONLY に変更します。

3.  RegEdit ユーティリティを使用して、"HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ DataFactory HandlerInfo" に移動し \\ **、HandlerRequired** が 0 に設定され **、DefaultHandler** が "" (Null 文字列) に設定されている必要があります。
    
    > [!NOTE]
    > [!メモ] レジストリのこのセクションを変更した場合は、コマンド プロンプトに「NET STOP W3SVC」および「NET START W3SVC」を入力して、World Wide Web Publishing Service の停止および再起動を行う必要があります。

4.  RegEdit ユーティリティを使用して、レジストリ内で "HKEY \_ \_ LOCAL MACHINE SYSTEM \\ \\ CurrentControlSet \\ Services \\ W3SVC \\ Parameters ADCLaunch" に移動し \\ **、RDSServer.Datafactory** と呼ばれるキーが用意されているのを確認します。 ない場合は、これを作成します。

5.  Internet Services Manager を使用して、既定の Web サイトに移動し、MSADC 仮想ルートのプロパティを表示します。 [ディレクトリ セキュリティ] タブの [IP アドレスとドメイン名の制限] を調べます。 アクセスを [拒否する] が選択されている場合は、[許可する] をクリックします。

変更しても問題が解決されない場合は、サーバーを再起動してください。

