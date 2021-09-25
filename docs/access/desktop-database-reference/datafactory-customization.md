---
title: DataFactory のカスタマイズ
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b69ed36acb84e12927d69fcb7b4df102a792f5d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585873"
---
# <a name="datafactory-customization"></a>DataFactory のカスタマイズ


**適用先**: Access 2013、Office 2013

リモート データ サービス (RDS) には、3 階層のクライアント/サーバー システムでデータ アクセスを簡単に行う手段があります。クライアントのデータ コントロールで、リモート データ ソース上でクエリを実行するための接続文字列とコマンド文字列のパラメーターを指定するか、または、更新を実行するための接続文字列と [Recordset](recordset-object-ado.md) オブジェクトのパラメーターを指定します。

パラメーターは、リモート データ ソースでデータ アクセス操作を実行するサーバー プログラムに渡されます。RDS には、[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトという既定のサーバー プログラムがあります。この **RDSServer.DataFactory** は、クエリで作成された **Recordset** オブジェクトをクライアントに返します。

ただし、 **RDSServer.DataFactory** が実行できるのは、クエリと更新に制限されています。接続文字列またはコマンド文字列の検証または処理は、実行できません。

ADO を使用すると **、DataFactory** がハンドラーと呼ばれる別の種類のサーバー プログラムと組み合わせて動作 *します。* The handler can modify client connection and command strings before they are used to access the data source. In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.

ハンドラーがクライアントのパラメーターとアクセス権の変更に使用するパラメーターは、カスタマイズ ファイルの各セクションに指定します。

**DataFactory** オブジェクトのカスタマイズの詳細については、次のトピックを参照してください。

- [カスタマイズ ファイルの概要](understanding-the-customization-file.md)
- [カスタマイズ ファイルの Connect セクション](customization-file-connect-section.md)
- [カスタマイズ ファイルの SQL セクション](customization-file-sql-section.md)
- [カスタマイズ ファイルの UserList セクション](customization-file-userlist-section.md)
- [カスタマイズ ファイルの Logs セクション](customization-file-logs-section.md)
- [クライアントで必要な設定](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [独自のカスタマイズされたハンドラーの作成](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
