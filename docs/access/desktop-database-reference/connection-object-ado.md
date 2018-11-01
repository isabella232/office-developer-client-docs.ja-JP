---
title: Connection オブジェクト (ADO)
TOCTitle: Connection Object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0f2c629a24bf6327be8a9848e719b40bfa88ea17
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873321"
---
# <a name="connection-object-ado"></a>Connection オブジェクト (ADO)

**適用されます**Access 2013、Office 2013。

データ ソースに対して開かれている接続を表します。

## <a name="remarks"></a>備考

**Connection** オブジェクトは、データ ソースとの固有のセッションを表します。クライアント/サーバー データベース システムの場合、このオブジェクトは、サーバーへの実際のネットワーク接続に相当します。プロバイダーがサポートする機能によっては、 **Connection** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。

**Connection** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。

  - 接続を開く前に、[ConnectionString](connectionstring-property-ado.md)、[ConnectionTimeout](connectiontimeout-property-ado.md)、および [Mode](mode-property-ado.md) の各プロパティを使用して接続を設定できます。 **ConnectionString** は **Connection** オブジェクトの既定のプロパティです。

  - [CursorLocation](cursorlocation-property-ado.md) プロパティをクライアントに設定して、バッチ更新をサポートする [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) を呼び出すことができます。

  - [DefaultDatabase](defaultdatabase-property-ado.md) プロパティを使用して、接続の既定のデータベースを設定できます。

  - [IsolationLevel](isolationlevel-property-ado.md) プロパティを使用して、接続上で開かれているトランザクションの分離レベルを設定できます。

  - [Provider](provider-property-ado.md) プロパティを使用して、OLE DB プロバイダーを指定できます。

  - [Open](open-method-ado-connection.md) メソッドと [Close](close-method-ado.md) メソッドを使用して、データ ソースへの物理的な接続を確立し、後で切断できます。

  - [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) メソッドを使用して接続上でコマンドを実行し、 [CommandTimeout](commandtimeout-property-ado.md) プロパティを使用して実行を設定できます。
    

    > [!NOTE]
    > [!メモ] Command オブジェクトを使用せずにクエリを実行するには、クエリ文字列を **Connection** オブジェクトの **Execute** メソッドに渡します。ただし、コマンド テキストを永続化して再実行するか、クエリ パラメーターを使用する場合は、 [Command](command-object-ado.md) オブジェクトが必要となります。

  - [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)、[CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)、[RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の各メソッドおよび [Attributes](attributes-property-ado.md) プロパティを使用して、開いている接続上のトランザクション (プロバイダーがネストされているトランザクションをサポートしている場合は、ネストされているトランザクションも含む) を管理できます。

  - [Errors](errors-collection-ado.md) コレクションを使用して、データ ソースから返されたエラーを調べることができます。

  - [Version](version-property-ado.md) プロパティを使用して、使用中の ADO 実装からバージョンを取得できます。

  - [OpenSchema](openschema-method-ado.md) メソッドを使用して、データベースのスキーマ情報を取得できます。

前に定義した他のオブジェクトと無関係に **Connection** オブジェクトを作成できます。

次に示すように、コマンドやストアド プロシージャを **Connection** オブジェクト固有のメソッドとして実行できます。

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>コマンドを Connection オブジェクト固有のメソッドとして実行する

コマンドを実行するには、 **Command** オブジェクトの [Name](name-property-ado.md) プロパティを使用して、コマンドに名前を設定します。 **Command** オブジェクトの **ActiveConnection** プロパティを該当する接続に設定します。次に、ステートメントを、コマンド名 ( **Connection** オブジェクトのメソッド名として)、パラメーター、 **Recordset** オブジェクト (行を取得する場合) の順に指定して発行します。 **Recordset** プロパティを設定して、結果の **Recordset** をカスタマイズします。次に例を示します。

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>ストアド プロシージャを Connection オブジェクト固有のメソッドとして実行する

ストアド プロシージャを実行するには、ステートメントを、ストアド プロシージャ名 ( **Connection** オブジェクトのメソッド名として)、パラメーターの順に指定して発行します。ADO では、パラメーターの種類について最適なものが推測されます。次に例を示します。

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
