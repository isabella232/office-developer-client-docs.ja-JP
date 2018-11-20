---
title: クエリ定義のメンバー (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6e62d302dc1164e70d83dcbb06ac56c21898b82
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026261"
---
# <a name="querydef-members-dao"></a><span data-ttu-id="bcac5-102">クエリ定義のメンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="bcac5-102">QueryDef members (DAO)</span></span>


<span data-ttu-id="bcac5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bcac5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bcac5-104">QueryDef オブジェクトは、Microsoft Access データベース エンジン データベースのクエリのストアド定義を表します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-104">A QueryDef object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="methods"></a><span data-ttu-id="bcac5-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="bcac5-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bcac5-106">名前</span><span class="sxs-lookup"><span data-stu-id="bcac5-106">Name</span></span></p></th>
<th><p><span data-ttu-id="bcac5-107">説明</span><span class="sxs-lookup"><span data-stu-id="bcac5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-109"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bcac5-109"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bcac5-110">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="bcac5-110">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bcac5-111">保留中の非同期メソッド呼び出しの実行をキャンセルします (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="bcac5-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-112"><strong><a href="querydef-close-method-dao.md">閉じる</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-112"><strong><a href="querydef-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-113">開いている <strong>QueryDef</strong> を閉じます。</span><span class="sxs-lookup"><span data-stu-id="bcac5-113">Closes an open <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-115">新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="bcac5-115">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-117">指定したオブジェクトの SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-117">Executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-118"><strong><a href="querydef-openrecordset-method-dao.md">何らか</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-119">新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成して <strong>Recordsets</strong> コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="bcac5-120">プロパティ</span><span class="sxs-lookup"><span data-stu-id="bcac5-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bcac5-121">名前</span><span class="sxs-lookup"><span data-stu-id="bcac5-121">Name</span></span></p></th>
<th><p><span data-ttu-id="bcac5-122">説明</span><span class="sxs-lookup"><span data-stu-id="bcac5-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p102">ローカル メモリにキャッシュされた ODBC データ ソースから取得したレコード数を設定または取得します。値の取得および設定が可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-p102">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p103">パススルー クエリで使用するデータベース ソースに関する情報を提供する値を設定します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-p103">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p104">オブジェクトを作成した日付と時刻を取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="bcac5-p104">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p105">指定したオブジェクトに格納されているすべての <strong><a href="fields-collection-dao.md">Field</a></strong> オブジェクトを表す <strong><a href="field-object-dao.md">Fields</a></strong> コレクションを取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="bcac5-p105">Returns a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection that represents all stored <strong><a href="field-object-dao.md">Field</a></strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p106">オブジェクトを最後に変更した日付および時刻を取得します。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="bcac5-p106">Returns the date and time of the most recent change made to an object. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-139">ODBC データ ソースに対して実行するクエリから返されるレコードの最大数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-139">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p107">指定したオブジェクトの名前を取得または設定します。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="bcac5-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-144">ODBC データベースに対して <strong><a href="querydef-object-dao.md">QueryDef</a></strong> を実行したときに、タイムアウト エラーが発生するまでの待ち時間を秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-144">Indicates the number of seconds to wait before a timeout error occurs when a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> is executed on an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-145"><strong><a href="querydef-parameters-property-dao.md">パラメーター</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-145"><strong><a href="querydef-parameters-property-dao.md">Parameters</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p108">指定した <a href="parameters-collection-dao.md">QueryDef</a> オブジェクトのすべての <a href="parameter-object-dao.md"><strong>Parameter</strong></a> オブジェクトが含まれた <strong><strong>Parameters</strong></strong> コレクションを取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="bcac5-p108">Returns a <strong><a href="parameters-collection-dao.md">Parameters</a></strong> collection that contains all of the <strong><a href="parameter-object-dao.md">Parameter</a></strong> objects of the specified <strong>QueryDef</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-149"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bcac5-149"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bcac5-150">Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="bcac5-150">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bcac5-p110">ODBC <strong>SQLPrepare</strong> API 関数を使用して、実行する前にクエリを一時的なストアド プロシージャとしてサーバーに準備する必要があるか、または ODBC <strong>SQLExecDirect</strong> API 関数を使用して、クエリを直接実行するかどうかを示す値を設定します (ODBCDirect ワークスペースのみ)。値の取得および設定が可能です。 <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong> クラスの定数を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-p110">Sets or returns a value that indicates whether the query should be prepared on the server as a temporary stored procedure, using the ODBC <strong>SQLPrepare</strong> API function, prior to execution, or just executed using the ODBC <strong>SQLExecDirect</strong> API function (ODBCDirect workspaces only). Read/Write <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p111">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="bcac5-p111">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-157">直前に呼び出された <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> メソッドの影響を受けるレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-157">Returns the number of records affected by the most recently invoked <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-159">外部データベースに対する SQL パススルー クエリでレコードを返すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="bcac5-159">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-161"><strong><a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトが実行するクエリを定義する SQL ステートメントを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-161">Sets or returns the SQL statement that defines the query executed by a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-163"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bcac5-163"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bcac5-164">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="bcac5-164">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bcac5-165">非同期操作 (つまり、 <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> オプションを指定して呼び出したメソッド) の実行が完了したかどうかを示します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="bcac5-165">Indicates whether or not an asynchronous operation (that is, a method called with the <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bcac5-166"><strong><a href="querydef-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-166"><strong><a href="querydef-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p113">オブジェクトの操作の種類またはデータ型を示す値を設定あるいは取得します。値の取得のみ可能です。整数型 (<strong>Integer</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcac5-p113">Sets or returns a value that indicates the operational type or data type of an object. Read-only<strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bcac5-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="bcac5-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bcac5-p114">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="bcac5-p114">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

