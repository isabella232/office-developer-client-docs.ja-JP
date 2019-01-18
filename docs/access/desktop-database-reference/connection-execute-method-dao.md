---
title: Connection.Execute メソッド (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8140dbe9bc0c68d467c011d77bc0c00cec7ad560
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709930"
---
# <a name="connectionexecute-method-dao"></a><span data-ttu-id="9505c-102">Connection.Execute メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="9505c-102">Connection.Execute method (DAO)</span></span>

<span data-ttu-id="9505c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9505c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9505c-104">指定したオブジェクトのアクション クエリまたは SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="9505c-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9505c-105">構文</span><span class="sxs-lookup"><span data-stu-id="9505c-105">Syntax</span></span>

<span data-ttu-id="9505c-106">*式*です。(***クエリ\*\*\*\*\*\*のオプション***) を実行します。</span><span class="sxs-lookup"><span data-stu-id="9505c-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="9505c-107">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="9505c-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9505c-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9505c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9505c-109">名前</span><span class="sxs-lookup"><span data-stu-id="9505c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9505c-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="9505c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9505c-111">データ型</span><span class="sxs-lookup"><span data-stu-id="9505c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9505c-112">説明</span><span class="sxs-lookup"><span data-stu-id="9505c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9505c-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="9505c-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="9505c-114">必須</span><span class="sxs-lookup"><span data-stu-id="9505c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="9505c-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-116">SQL ステートメントまたは <strong>QueryDef</strong> オブジェクトの <strong>Name</strong> プロパティの値を示す文字列型 (<strong>String</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="9505c-116">A <strong>String</strong> that is an SQL statement or the <strong>Name</strong> property value of a <strong>QueryDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9505c-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="9505c-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="9505c-118">省略可能</span><span class="sxs-lookup"><span data-stu-id="9505c-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="9505c-119"><strong>Variant (バリアント型)</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-120">[設定] で指定された、クエリのデータ整合性の特性を表す定数 (または定数の組み合わせ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-120">A constant or combination of constants that determines the data integrity characteristics of the query, as specified in Settings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9505c-121">注釈</span><span class="sxs-lookup"><span data-stu-id="9505c-121">Remarks</span></span>

<span data-ttu-id="9505c-122">**[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** 定数は、次は、オプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9505c-122">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9505c-123">定数</span><span class="sxs-lookup"><span data-stu-id="9505c-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="9505c-124">説明</span><span class="sxs-lookup"><span data-stu-id="9505c-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9505c-125"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-125"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-126">他のユーザーに対して書き込み権限を許可しません (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-126">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9505c-127"><strong>組み合わせて</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-127"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-128">(既定値) 矛盾した更新を実行します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-128">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9505c-129"><strong>指定できます。</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-129"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-130">一貫性のある更新を実行します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-130">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9505c-131"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-131"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-p101">SQL パススルー クエリを実行します。このオプションを設定すると、SQL ステートメントが ODBC データベースに渡されて処理されます (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9505c-134"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-134"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-135">エラーが発生した場合、更新をロールバックします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-135">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9505c-136"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-136"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-137">編集中のデータが他のユーザーによって変更されている場合、実行時エラーを生成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-137">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9505c-138"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-138"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-139">クエリを非同期に実行します (ODBCDirect の Connection オブジェクトと QueryDef オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-139">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9505c-140"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="9505c-140"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="9505c-141">SQLPrepare ODBC API 関数を呼び出さずにステートメントを実行します (ODBCDirect の Connection オブジェクトと QueryDef オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="9505c-141">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9505c-p102">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="9505c-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="9505c-p103">[!メモ] 定数 **dbConsistent** と **dbInconsistent** は互いに排他的です。1 つの **OpenRecordset** のインスタンスにおいては、どちらか一方を使用できますが、両方を使用することはできません。 **dbConsistent** と **dbInconsistent** の両方を使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9505c-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="9505c-p104">**Execute** メソッドはアクション クエリでのみ有効です。別の種類のクエリで **Execute** を使用すると、エラーが発生します。アクション クエリはレコードを返さないので、 **Execute** は **Recordset** を返しません。 **Recordset** が返されない場合は、ODBCDirect ワークスペースで SQL パススルー クエリを実行してもエラーは返されません。</span><span class="sxs-lookup"><span data-stu-id="9505c-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="9505c-p105">**Connection** 、 **Database** 、または **QueryDef** のオブジェクトの **RecordsAffected** プロパティを使用して、最後に使用された **Execute** メソッドによって影響を受けたレコードの数を取得できます。たとえば、アクション クエリの実行時に削除、更新、または挿入されたレコードの数が **RecordsAffected** に格納されます。 **Execute** メソッドを使用してクエリを実行すると、 **QueryDef** オブジェクトの **RecordsAffected** プロパティは、影響を受けたレコードの数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9505c-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="9505c-p106">Microsoft Access ワークスペースでは、指定した SQL ステートメントの構文が正しく、ユーザーが適切な権限を持っている場合、1 行も変更または削除できなくても、 **Execute** メソッドが失敗することはありません。したがって、 **Execute** メソッドを使って更新または削除のクエリを実行するときは、必ず **dbFailOnError** オプションを指定してください。このオプションを使用すると、影響を受けるレコードの一部がロックされているために更新または削除できない場合、実行時エラーが生成され、既に成功している変更もすべてロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="9505c-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="9505c-p107">以前のバージョンの Microsoft Jet データベース エンジンでは、暗黙のトランザクション内に自動的に SQL ステートメントが埋め込まれていました。 **dbFailOnError** を指定して実行したステートメントの一部が失敗した場合は、ステートメント全体がロールバックされました。パフォーマンスを向上するために、バージョン 3.5 以降では、この暗黙のトランザクションが取り除かれました。古いバージョンの DAO コードを更新する場合は、 **Execute** ステートメントの前後で明示的なトランザクションを使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="9505c-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="9505c-p108">Microsoft Access ワークスペースでのパフォーマンスを最適にする (特にマルチユーザー環境の場合) には、トランザクション内部に **Execute** メソッドをネストします。現在の **Workspace** オブジェクトの **BeginTrans** メソッドを使用し、次に **Execute** メソッドを使用し、最後に **Workspace** の **CommitTrans** メソッドを使用してトランザクションを完了します。これにより、変更がディスクに保存され、クエリ実行中に適用されていたロックがすべて解除されます。</span><span class="sxs-lookup"><span data-stu-id="9505c-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

