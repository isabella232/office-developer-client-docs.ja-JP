---
title: Command オブジェクト (ADO)
TOCTitle: Command Object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 48f30471dd5df224e8fe01538dc02d85ded54d6a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477210"
---
# <a name="command-object-ado"></a><span data-ttu-id="91eb1-102">Command オブジェクト (ADO)</span><span class="sxs-lookup"><span data-stu-id="91eb1-102">Command Object (ADO)</span></span>


<span data-ttu-id="91eb1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="91eb1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="91eb1-104">データ ソースに対して実行する特定のコマンドを定義します。</span><span class="sxs-lookup"><span data-stu-id="91eb1-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="91eb1-105">備考</span><span class="sxs-lookup"><span data-stu-id="91eb1-105">Remarks</span></span>

<span data-ttu-id="91eb1-p101">**Command** オブジェクトを使用すると、データベースに対してクエリを実行して [Recordset](recordset-object-ado.md) オブジェクトのレコードを取得したり、一括操作を実行したり、データベースの構造を操作したりできます。プロバイダーの機能によっては、 **Command** の一部のコレクション、メソッド、またはプロパティを参照すると、エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="91eb1-p101">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database. Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="91eb1-108">**Command** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="91eb1-109">[CommandText](commandtext-property-ado.md) プロパティを使用して、コマンドの実行可能なテキスト (SQL ステートメント) を定義できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="91eb1-110">[Parameter](parameter-object-ado.md) オブジェクトと [Parameters](parameters-collection-ado.md) コレクションを使用して、パラメーター化されたクエリまたはストアド プロシージャの引数を定義できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="91eb1-111">**Execute** メソッドを使用して、コマンドを実行し、必要に応じて [Recordset](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) オブジェクトを取得できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-111">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

  - <span data-ttu-id="91eb1-112">[CommandType](commandtype-property-ado.md) プロパティを使用して、コマンドを実行する前にそのコマンドの種類を指定し、パフォーマンスを向上できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-112">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="91eb1-113">[Prepared](prepared-property-ado.md) プロパティを使用して、コマンドの実行前に、プロバイダーがそのコマンドの準備された (コンパイル済みの) バージョンを保存するかどうかを制御できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-113">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="91eb1-114">[CommandTimeout](commandtimeout-property-ado.md) プロパティを使用して、コマンドの実行までプロバイダーが待機する時間を秒数で設定できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-114">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="91eb1-115">**Command** オブジェクトの [ActiveConnection](activeconnection-property-ado.md) プロパティを使用して、開いている接続をそのオブジェクトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-115">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="91eb1-116">[Name](name-property-ado.md) プロパティを設定して、 **Command** オブジェクトを関連付けられている [Connection](connection-object-ado.md) オブジェクトのメソッドとして識別できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-116">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="91eb1-117">**Command** オブジェクトを [Recordset](source-property-ado-recordset.md) の **Source** プロパティに渡すことにより、データを取得できます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-117">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="91eb1-118">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有の属性にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-118">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="91eb1-p102">[!メモ] <STRONG>Command</STRONG> オブジェクトを使用せずにクエリを実行するには、クエリ文字列を <A href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Connection</A> オブジェクトの <STRONG>Execute</STRONG> メソッド、または <A href="open-method-ado-recordset.md">Recordset</A> オブジェクトの <STRONG>Open</STRONG> メソッドに渡します。ただし、コマンド テキストを永続化して再実行するか、クエリ パラメーターを使用する場合は、 <STRONG>Command</STRONG> オブジェクトが必要となります。</span><span class="sxs-lookup"><span data-stu-id="91eb1-p102">To execute a query without using a <STRONG>Command</STRONG> object, pass a query string to the <A href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</A> method of a <STRONG>Connection</STRONG> object or to the <A href="open-method-ado-recordset.md">Open</A> method of a <STRONG>Recordset</STRONG> object. However, a <STRONG>Command</STRONG> object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span></P>



<span data-ttu-id="91eb1-p103">前に定義した **Connection** オブジェクトと無関係に **Command** オブジェクトを作成するには、その **ActiveConnection** プロパティを有効な接続文字列に設定します。その場合でも **Connection** オブジェクトは ADO によって作成されますが、オブジェクト変数に割り当てられることはありません。ただし、複数の **Command** オブジェクトを同一の接続に関連付ける場合は、明示的に **Connection** オブジェクトを作成して開く必要があります。こうすることで、 **Connection** オブジェクトがオブジェクト変数に割り当てられます。 **Command** オブジェクトの **ActiveConnection** プロパティをこのオブジェクト変数に設定しなかった場合、同じ接続文字列を使用しても、ADO によって各 **Command** オブジェクトに新しい **Connection** オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="91eb1-p103">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string. ADO still creates a **Connection** object, but it doesn't assign that object to an object variable. However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable. If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="91eb1-p104">**Command** を実行するには、関連する [Connection](name-property-ado.md) オブジェクトの該当する **Name** プロパティを使用して呼び出します。 **Command** では、その **ActiveConnection** プロパティを **Connection** オブジェクトに設定する必要があります。 **Command** にパラメーターがある場合は、その値を引数としてメソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="91eb1-p104">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object. The **Command** must have its **ActiveConnection** property set to the **Connection** object. If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="91eb1-p105">同じ接続で複数の **Command** オブジェクトを実行し、いずれかの **Command** オブジェクトが出力パラメーターを持つストアド プロシージャの場合、エラーが発生します。各 **Command** オブジェクトを実行するには、別の接続を使用するか、接続から他のすべての **Command** オブジェクトを切断します。</span><span class="sxs-lookup"><span data-stu-id="91eb1-p105">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs. To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="91eb1-p106">**Parameters** コレクションは **Command** オブジェクトの既定のメンバーです。結果として、次の 2 つのコード ステートメントは同じになります。</span><span class="sxs-lookup"><span data-stu-id="91eb1-p106">The **Parameters** collection is the default member of the **Command** object. As a result, the following two code statements are equivalent.</span></span>
