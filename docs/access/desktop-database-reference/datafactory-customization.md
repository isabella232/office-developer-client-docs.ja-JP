---
title: DataFactory のカスタマイズ
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5fc1c284ee7aae77c4fb067ad57d50200119594
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700025"
---
# <a name="datafactory-customization"></a>DataFactory のカスタマイズ


**適用されます**Access 2013、Office 2013。

リモート データ サービス (RDS) には、3 階層のクライアント/サーバー システムでデータ アクセスを簡単に行う手段があります。クライアントのデータ コントロールで、リモート データ ソース上でクエリを実行するための接続文字列とコマンド文字列のパラメーターを指定するか、または、更新を実行するための接続文字列と [Recordset](recordset-object-ado.md) オブジェクトのパラメーターを指定します。

パラメーターは、リモート データ ソースでデータ アクセス操作を実行するサーバー プログラムに渡されます。RDS には、[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトという既定のサーバー プログラムがあります。この **RDSServer.DataFactory** は、クエリで作成された **Recordset** オブジェクトをクライアントに返します。

ただし、 **RDSServer.DataFactory** が実行できるのは、クエリと更新に制限されています。接続文字列またはコマンド文字列の検証または処理は、実行できません。

ADO では、 **DataFactory**の作業別の種類のサーバー プログラムと連携して、*ハンドラー*が呼び出されることを指定できます。 ハンドラーでは、データ ソースへのアクセスに使用されるようにクライアントの接続文字列とコマンド文字列を変更できます。 さらに、ハンドラーは、データ ソースにデータを読み書きするクライアントの権限を制御するアクセス権を適用できます。

ハンドラーがクライアントのパラメーターとアクセス権の変更に使用するパラメーターは、カスタマイズ ファイルの各セクションに指定します。

**DataFactory** オブジェクトのカスタマイズの詳細については、次のトピックを参照してください。

- [カスタマイズ ファイルの概要](understanding-the-customization-file.md)
- [カスタマイズ ファイルの接続] セクション](customization-file-connect-section.md)
- [カスタマイズ ファイルの SQL セクション](customization-file-sql-section.md)
- [カスタマイズ ファイルの UserList セクション](customization-file-userlist-section.md)
- [カスタマイズ ファイルの Logs セクション](customization-file-logs-section.md)
- [クライアントで必要な設定](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [独自のカスタマイズされたハンドラーを記述します。](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
