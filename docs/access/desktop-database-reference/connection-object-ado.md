---
title: Connection オブジェクト (ADO)
TOCTitle: Connection object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7f35c2f76ec8cf2fd671f5ef9eefb42f8555237
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931387"
---
# <a name="connection-object-ado"></a><span data-ttu-id="b5994-102">Connection オブジェクト (ADO)</span><span class="sxs-lookup"><span data-stu-id="b5994-102">Connection object (ADO)</span></span>

<span data-ttu-id="b5994-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b5994-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5994-104">データ ソースに対して開かれている接続を表します。</span><span class="sxs-lookup"><span data-stu-id="b5994-104">Represents an open connection to a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5994-105">備考</span><span class="sxs-lookup"><span data-stu-id="b5994-105">Remarks</span></span>

<span data-ttu-id="b5994-p101">**Connection** オブジェクトは、データ ソースとの固有のセッションを表します。クライアント/サーバー データベース システムの場合、このオブジェクトは、サーバーへの実際のネットワーク接続に相当します。プロバイダーがサポートする機能によっては、 **Connection** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5994-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it may be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object may not be available.</span></span>

<span data-ttu-id="b5994-109">**Connection** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-109">With the collections, methods, and properties of a **Connection** object, you can do the following:</span></span>

  - <span data-ttu-id="b5994-p102">接続を開く前に、[ConnectionString](connectionstring-property-ado.md)、[ConnectionTimeout](connectiontimeout-property-ado.md)、および [Mode](mode-property-ado.md) の各プロパティを使用して接続を設定できます。 **ConnectionString** は **Connection** オブジェクトの既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="b5994-p102">Configure the connection before opening it with the [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md), and [Mode](mode-property-ado.md) properties. **ConnectionString** is the default property of the **Connection** object.</span></span>

  - <span data-ttu-id="b5994-112">[CursorLocation](cursorlocation-property-ado.md) プロパティをクライアントに設定して、バッチ更新をサポートする [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="b5994-112">Set the [CursorLocation](cursorlocation-property-ado.md) property to client to invoke the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), which supports batch updates.</span></span>

  - <span data-ttu-id="b5994-113">[DefaultDatabase](defaultdatabase-property-ado.md) プロパティを使用して、接続の既定のデータベースを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-113">Set the default database for the connection with the [DefaultDatabase](defaultdatabase-property-ado.md) property.</span></span>

  - <span data-ttu-id="b5994-114">[IsolationLevel](isolationlevel-property-ado.md) プロパティを使用して、接続上で開かれているトランザクションの分離レベルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-114">Set the level of isolation for the transactions opened on the connection with the [IsolationLevel](isolationlevel-property-ado.md) property.</span></span>

  - <span data-ttu-id="b5994-115">[Provider](provider-property-ado.md) プロパティを使用して、OLE DB プロバイダーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-115">Specify an OLE DB provider with the [Provider](provider-property-ado.md) property.</span></span>

  - <span data-ttu-id="b5994-116">[Open](open-method-ado-connection.md) メソッドと [Close](close-method-ado.md) メソッドを使用して、データ ソースへの物理的な接続を確立し、後で切断できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-116">Establish, and later break, the physical connection to the data source with the [Open](open-method-ado-connection.md) and [Close](close-method-ado.md) methods.</span></span>

  - <span data-ttu-id="b5994-117">[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) メソッドを使用して接続上でコマンドを実行し、 [CommandTimeout](commandtimeout-property-ado.md) プロパティを使用して実行を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-117">Execute a command on the connection with the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method and configure the execution with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="b5994-p103">[!メモ] Command オブジェクトを使用せずにクエリを実行するには、クエリ文字列を **Connection** オブジェクトの **Execute** メソッドに渡します。ただし、コマンド テキストを永続化して再実行するか、クエリ パラメーターを使用する場合は、 [Command](command-object-ado.md) オブジェクトが必要となります。</span><span class="sxs-lookup"><span data-stu-id="b5994-p103">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object. However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

  - <span data-ttu-id="b5994-120">[BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)、[CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)、[RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の各メソッドおよび [Attributes](attributes-property-ado.md) プロパティを使用して、開いている接続上のトランザクション (プロバイダーがネストされているトランザクションをサポートしている場合は、ネストされているトランザクションも含む) を管理できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-120">Manage transactions on the open connection, including nested transactions if the provider supports them, with the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), and [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) methods and the [Attributes](attributes-property-ado.md) property.</span></span>

  - <span data-ttu-id="b5994-121">[Errors](errors-collection-ado.md) コレクションを使用して、データ ソースから返されたエラーを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="b5994-121">Examine errors returned from the data source with the [Errors](errors-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="b5994-122">[Version](version-property-ado.md) プロパティを使用して、使用中の ADO 実装からバージョンを取得できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-122">Read the version from the ADO implementation used with the [Version](version-property-ado.md) property.</span></span>

  - <span data-ttu-id="b5994-123">[OpenSchema](openschema-method-ado.md) メソッドを使用して、データベースのスキーマ情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-123">Obtain schema information about your database with the [OpenSchema](openschema-method-ado.md) method.</span></span>

<span data-ttu-id="b5994-124">前に定義した他のオブジェクトと無関係に **Connection** オブジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-124">You can create **Connection** objects independently of any other previously defined object.</span></span>

<span data-ttu-id="b5994-125">次に示すように、コマンドやストアド プロシージャを **Connection** オブジェクト固有のメソッドとして実行できます。</span><span class="sxs-lookup"><span data-stu-id="b5994-125">You can execute commands or stored procedures as if they were native methods on the **Connection** object, as illustrated below.</span></span>

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="b5994-126">コマンドを Connection オブジェクト固有のメソッドとして実行する</span><span class="sxs-lookup"><span data-stu-id="b5994-126">Execute a command as a native method of a Connection object</span></span>

<span data-ttu-id="b5994-p104">コマンドを実行するには、 **Command** オブジェクトの [Name](name-property-ado.md) プロパティを使用して、コマンドに名前を設定します。 **Command** オブジェクトの **ActiveConnection** プロパティを該当する接続に設定します。次に、ステートメントを、コマンド名 ( **Connection** オブジェクトのメソッド名として)、パラメーター、 **Recordset** オブジェクト (行を取得する場合) の順に指定して発行します。 **Recordset** プロパティを設定して、結果の **Recordset** をカスタマイズします。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b5994-p104">To execute a command, give the command a name using the **Command** object [Name](name-property-ado.md) property. Set the **Command** object's **ActiveConnection** property to the connection. Then issue a statement where the command name is used as if it were a method on the **Connection** object, followed by any parameters, then followed by a **Recordset** object if any rows are returned. Set the **Recordset** properties to customize the resulting **Recordset**. For example:</span></span>

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

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="b5994-132">ストアド プロシージャを Connection オブジェクト固有のメソッドとして実行する</span><span class="sxs-lookup"><span data-stu-id="b5994-132">Execute a stored procedure as a native method of a Connection object</span></span>

<span data-ttu-id="b5994-p105">ストアド プロシージャを実行するには、ステートメントを、ストアド プロシージャ名 ( **Connection** オブジェクトのメソッド名として)、パラメーターの順に指定して発行します。ADO では、パラメーターの種類について最適なものが推測されます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b5994-p105">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the **Connection** object, followed by any parameters. ADO will make a "best guess" of parameter types. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
