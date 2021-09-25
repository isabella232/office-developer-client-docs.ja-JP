---
title: DataFactory をセーフ モードまたはアクセス制限なしモードで構成する
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aa371dd98d61bd23b33c83bf4ce9b78947e10600
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577564"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>DataFactory をセーフ モードまたはアクセス制限なしモードで構成する


**適用先:** Access 2013、Office 2013

既定では、ADO は "安全な" [RDSServer.DataFactory](datafactory-object-rdsserver.md) 構成でインストールされます。RDS Server コンポーネントのセーフ モードの条件は次のとおりです。

1.  RDSServer.DataFactory にハンドラーが必須である (必須かどうかは、レジストリ キーの設定によって決まります)。

2.  既定のハンドラーである msdfmap.handler が登録され、安全なハンドラーの一覧にあり、既定のハンドラーとしてマークされている。

3.  Windows ディレクトリに msdfmap.ini ファイルがインストールされている。3 層モードで RDS を使用する場合は、必要に応じてこのファイルを事前に設定する必要があります。

または、アクセス制限なしの **DataFactory** インストールを構成することもできます。 **DataFactory** は、カスタム ハンドラーがなくても直接使用できます。 接続文字列を変更してカスタム ハンドラーを使うことができますが、そうする必要はありません。 **RDSServer.DataFactory** オブジェクトを使用する場合の影響の詳細については [、「Securing RDS Applications」を参照してください](securing-rds-applications.md)。

安全に構成を行うために、レジストリ ファイル handsafe.reg がハンドラー レジストリ エントリのセットアップ用に用意されています。セーフ モードで実行するには、handsafe.reg を実行します。アクセス制限なしの構成を行うためには、レジストリ ファイル handunsf.reg がハンドラー レジストリ エントリのセットアップ用に用意されています。アクセス制限なしモードで実行するには、handunsf.reg を実行します。

handsafe.reg または handunsf.reg のいずれかを実行した後、コマンド ウィンドウに「NET STOP W3SVC」と「NET START W3SVC」というコマンドを入力して、Web サーバー上で World Wide Web Publishing Service を停止して再起動する必要があります。

RDS のカスタム ハンドラー機能の使用方法の詳細については、技術記事「Using the Customization Handler Feature in RDS 2.1」 (英語) を参照してください。

