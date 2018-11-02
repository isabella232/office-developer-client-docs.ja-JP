---
title: DBEngine.Idle メソッド (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d750bd39835a8bb69d195663b72254d3f53cd635
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926081"
---
# <a name="dbengineidle-method-dao"></a><span data-ttu-id="586ef-102">DBEngine.Idle メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="586ef-102">DBEngine.Idle method (DAO)</span></span>


<span data-ttu-id="586ef-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="586ef-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="586ef-104">データの処理を中断し、Microsoft Access データベース エンジンでメモリの最適化やページのタイムアウトなどのタスクを完了できるようにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="586ef-104">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="586ef-105">構文</span><span class="sxs-lookup"><span data-stu-id="586ef-105">Syntax</span></span>

<span data-ttu-id="586ef-106">*式*です。アイドル (***アクション***)</span><span class="sxs-lookup"><span data-stu-id="586ef-106">*expression* .Idle(***Action***)</span></span>

<span data-ttu-id="586ef-107">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="586ef-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="586ef-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="586ef-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="586ef-109">名前</span><span class="sxs-lookup"><span data-stu-id="586ef-109">Name</span></span></p></th>
<th><p><span data-ttu-id="586ef-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="586ef-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="586ef-111">データ型</span><span class="sxs-lookup"><span data-stu-id="586ef-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="586ef-112">説明</span><span class="sxs-lookup"><span data-stu-id="586ef-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="586ef-113">アクション</span><span class="sxs-lookup"><span data-stu-id="586ef-113">Action</span></span></p></td>
<td><p><span data-ttu-id="586ef-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="586ef-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="586ef-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="586ef-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="586ef-p101">実行するアクションを指定します。指定できる定数は、<strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> クラスの定数のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="586ef-p101">Specifies the action to take. Can be one of the <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="586ef-118">注釈</span><span class="sxs-lookup"><span data-stu-id="586ef-118">Remarks</span></span>

<span data-ttu-id="586ef-p102">**Idle** メソッドを使用すると、データ処理の負荷が高いために最新の状態でない可能性のあるバックグラウンド タスクを Microsoft Access データベース エンジンで実行できるようになります。たとえば、マルチユーザー/マルチタスキングの環境で、 **[Recordset](recordset-object-dao.md)** 内のすべてのレコードを最新の状態に保つためのバックグラウンド処理に必要な時間が十分でない場合に、データが最新の状態でないことがあります。</span><span class="sxs-lookup"><span data-stu-id="586ef-p102">The **Idle** method allows the Microsoft Access database engine to perform background tasks that may not be up-to-date because of intense data processing. This is often true in multiuser, multitasking environments that don't have enough background processing time to keep all records in a **[Recordset](recordset-object-dao.md)** current.</span></span>

<span data-ttu-id="586ef-p103">通常は、他のアクション (マウスの移動を含む) が発生していない場合のみ、読み取りロックが解除され、ローカルにあるダイナセット タイプの **Recordset** オブジェクトのデータが更新されます。 **Idle** メソッドを定期的に使用すると、不要な読み取りロックが解除され、バックグラウンド処理のタスクの遅れを取り戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="586ef-p103">Usually, read locks are removed and data in local dynaset-type **Recordset** objects are updated only when no other actions (including mouse movements) occur. If you periodically use the **Idle** method, the Microsoft Access database engine can catch up on background processing tasks by releasing unneeded read locks.</span></span>

<span data-ttu-id="586ef-123">任意指定の引数 **dbRefreshCache** を指定すると、データベースの最新のデータのみを使用してメモリが更新されます。</span><span class="sxs-lookup"><span data-stu-id="586ef-123">Specifying the optional **dbRefreshCache** argument refreshes memory with only the most current data from the database.</span></span>

<span data-ttu-id="586ef-p104">シングルユーザー環境の場合は、1 つのアプリケーションの複数のインスタンスを実行していない限り、このメソッドを使用する必要はありません。 **Idle** メソッドを使用すると、メモリのロックが解除され、データが強制的にディスクに書き込まれるため、マルチユーザー環境の場合はこのメソッドを使用することによりパフォーマンスが向上することがあります。</span><span class="sxs-lookup"><span data-stu-id="586ef-p104">You don't need to use this method in single-user environments unless multiple instances of an application are running. The **Idle** method may increase performance in a multiuser environment because it forces the database engine to write data to disk, releasing locks on memory.</span></span>


> [!NOTE]
> <span data-ttu-id="586ef-126">[!メモ] 操作をトランザクションの一部にすることにより、読み取りロックを解除することもできます。</span><span class="sxs-lookup"><span data-stu-id="586ef-126">You can also release read locks by making operations part of a transaction.</span></span>

## <a name="example"></a><span data-ttu-id="586ef-127">例</span><span class="sxs-lookup"><span data-stu-id="586ef-127">Example</span></span>

<span data-ttu-id="586ef-p105">次の使用例では、 **Idle** メソッドを使用して、出力プロシージャがデータベースの最新のデータにアクセスできるようにします。このプロシージャを実行するには、IdleOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="586ef-p105">This example uses the **Idle** method to ensure that an output procedure is accessing the most current data available from the database. The IdleOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

