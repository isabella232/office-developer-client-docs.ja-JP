---
title: DataFactory をセーフ モードまたはアクセス制限なしモードで構成する
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04964b085d6ece60bbdb30e4561e6e02de76268d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863935"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>DataFactory をセーフ モードまたはアクセス制限なしモードで構成する


**適用されます**Access 2013 |。Office 2013

既定では、ADO は "安全な" [RDSServer.DataFactory](datafactory-object-rdsserver.md) 構成でインストールされます。RDS Server コンポーネントのセーフ モードの条件は次のとおりです。

1.  RDSServer.DataFactory にハンドラーが必須である (必須かどうかは、レジストリ キーの設定によって決まります)。

2.  既定のハンドラーである msdfmap.handler が登録され、安全なハンドラーの一覧にあり、既定のハンドラーとしてマークされている。

3.  Windows ディレクトリに msdfmap.ini ファイルがインストールされている。3 層モードで RDS を使用する場合は、必要に応じてこのファイルを事前に設定する必要があります。

または、アクセス制限なしの **DataFactory** インストールを構成することもできます。 **DataFactory** は、カスタム ハンドラーがなくても直接使用できます。 接続文字列を変更してカスタム ハンドラーを使うことができますが、そうする必要はありません。 **RDSServer.DataFactory**オブジェクトを使用する場合の影響の詳細については、 [RDS アプリケーションをセキュリティで保護する](securing-rds-applications.md)を参照してください。

安全に構成を行うために、レジストリ ファイル handsafe.reg がハンドラー レジストリ エントリのセットアップ用に用意されています。セーフ モードで実行するには、handsafe.reg を実行します。アクセス制限なしの構成を行うためには、レジストリ ファイル handunsf.reg がハンドラー レジストリ エントリのセットアップ用に用意されています。アクセス制限なしモードで実行するには、handunsf.reg を実行します。

<<<<<<< ヘッド handsafe.reg または handunsf.reg というのいずれかを実行した後、停止して Web サーバー上の World Wide Web 発行サービスを再起動するには、コマンド ウィンドウで次のコマンドを入力:「NET W3SVC を停止」と「ネット スタート W3SVC」です。
=== Handsafe.reg または handunsf.reg というのいずれかを実行して後に、する必要がありますを停止して web サーバー上の World Wide Web 発行サービスを再起動するには、コマンド ウィンドウで次のコマンドを入力:「NET W3SVC を停止」と「ネット スタート W3SVC」です。
>>>>>>> master

RDS のカスタム ハンドラー機能の使用方法の詳細については、技術記事「Using the Customization Handler Feature in RDS 2.1」 (英語) を参照してください。

