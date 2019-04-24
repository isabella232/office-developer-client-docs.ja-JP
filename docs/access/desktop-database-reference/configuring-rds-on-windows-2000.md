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
# <a name="configuring-rds-on-windows-2000"></a>Windows 2000 での RDS の構成


**適用先:** Access 2013、Office 2013

Windows 2000 へのアップグレード後に RDS が正しく機能しない場合は、次の手順に従って問題のトラブルシューティングを行ってください。

1.  World Wide Web Publishing Service が最初に実行されていることを確認するために、Internet Explorer を使用して https://*サーバー*に移動します。 If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".

2.  [スタート] ボタンをクリックし、[ファイル名を指定して実行] をクリックします。 「msdfmap.ini」と入力して [OK] をクリックし、メモ帳で msdfmap.ini ファイルを開きます。 [ \[CONNECT DEFAULT\] ] セクションをチェックし、ACCESS パラメーターが NOACCESS に設定されている場合は、READONLY に変更します。

3.  RegEdit ユーティリティを使用して、"HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\ハンドラ info" に移動し、**ハンドラ required**が0に設定されていること、および**defaulthandler**が "" になっていることを確認します (Null文字列)。
    
    > [!NOTE]
    > [!メモ] レジストリのこのセクションを変更した場合は、コマンド プロンプトに「NET STOP W3SVC」および「NET START W3SVC」を入力して、World Wide Web Publishing Service の停止および再起動を行う必要があります。

4.  RegEdit ユーティリティを使用して、レジストリ内を移動し\_、\_"\\HKEY\\LOCAL\\MACHINE\\SYSTEM\\CurrentControlSet\\service W3SVC Parameters ADCLaunch" という**キーがあるかどうかを確認します。rdsserver.datafactory。 Datafactory** ない場合は、これを作成します。

5.  インターネットサービスマネージャーを使用して、既定の web サイトに移動し、MSADC 仮想ルートのプロパティを表示します。 [ディレクトリ セキュリティ] タブの [IP アドレスとドメイン名の制限] を調べます。 アクセスを [拒否する] が選択されている場合は、[許可する] をクリックします。

変更しても問題が解決されない場合は、サーバーを再起動してください。

