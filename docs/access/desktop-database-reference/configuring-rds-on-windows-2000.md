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
# <a name="configuring-rds-on-windows-2000"></a>Windows 2000 に RDS を構成する


**適用されます**Access 2013 |。Office 2013

Windows 2000 へのアップグレード後に RDS が正しく機能しない場合は、次の手順に従って問題のトラブルシューティングを行ってください。

1.  World Wide Web 発行サービスが実行されている最初 Internet Explorer を使用して、https://*サーバー*に移動することを確認します。 このように web サーバーにアクセスできない場合は、コマンド プロンプトに移動し、次のコマンドでは、「NET スタート W3SVC」を入力します。

2.  [スタート] ボタンをクリックし、[ファイル名を指定して実行] をクリックします。 「msdfmap.ini」と入力して [OK] をクリックし、メモ帳で msdfmap.ini ファイルを開きます。 チェック、\[既定の接続\]セクション、およびアクセスのパラメーターは、NOACCESS に設定されている場合は読み取り専用に変更します。

3.  RegEdit ユーティリティを使用してに移動"HKEY\_ローカル\_マシン\\ソフトウェア\\Microsoft\\DataFactory\\HandlerInfo" **HandlerRequired**が 0 に設定され、 **DefaultHandler**がかどうかを確認し、""(Null文字列) です。
    

    > [!NOTE]
    > <P>[!メモ] レジストリのこのセクションを変更した場合は、コマンド プロンプトに「NET STOP W3SVC」および「NET START W3SVC」を入力して、World Wide Web Publishing Service の停止および再起動を行う必要があります。</P>



4.  レジストリ内を移動する、レジストリ エディター ユーティリティを使用して"HKEY\_ローカル\_マシン\\システム\\CurrentControlSet\\サービス\\W3SVC\\パラメーター\\ADCLaunch] キーと呼ばれる**があることを確認し、RDSServer.Datafactory**。 ない場合は、これを作成します。

5.  インターネット サービス マネージャーを使用して既定の Web サイトに移動し、MSADC 仮想ルートのプロパティを表示します。[ディレクトリ セキュリティ] タブの [IP アドレスとドメイン名の制限] を調べます。アクセスを [拒否する] が選択されている場合は、[許可する] をクリックします。

変更しても問題が解決されない場合は、サーバーを再起動してください。

