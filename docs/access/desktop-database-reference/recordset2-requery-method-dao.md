---
title: Recordset2.Requery メソッド (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7019b0e4d3ffa916aea8436db14f3a8476f2e36f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476272"
---
# <a name="recordset2requery-method-dao"></a><span data-ttu-id="f0b83-102">Recordset2.Requery メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="f0b83-102">Recordset2.Requery Method (DAO)</span></span>


<span data-ttu-id="f0b83-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0b83-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f0b83-104">**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行することにより、オブジェクト内のデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="f0b83-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b83-105">構文</span><span class="sxs-lookup"><span data-stu-id="f0b83-105">Syntax</span></span>

<span data-ttu-id="f0b83-106">*式*です。(***NewQueryDef***) のクエリを再実行します。</span><span class="sxs-lookup"><span data-stu-id="f0b83-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="f0b83-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f0b83-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f0b83-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f0b83-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0b83-109">名前</span><span class="sxs-lookup"><span data-stu-id="f0b83-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f0b83-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="f0b83-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f0b83-111">データ型</span><span class="sxs-lookup"><span data-stu-id="f0b83-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f0b83-112">説明</span><span class="sxs-lookup"><span data-stu-id="f0b83-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0b83-113">NewQueryDef</span><span class="sxs-lookup"><span data-stu-id="f0b83-113">NewQueryDef</span></span></p></td>
<td><p><span data-ttu-id="f0b83-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="f0b83-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="f0b83-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="f0b83-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f0b83-116"><a href="querydef-object-dao.md"><strong>QueryDef</strong></a> オブジェクトの <strong>Name</strong> プロパティの値を表します。</span><span class="sxs-lookup"><span data-stu-id="f0b83-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f0b83-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f0b83-117">Remarks</span></span>

<span data-ttu-id="f0b83-118">このメソッドは、 **Recordset** に確実に最新のデータが含まれるようにするために使用します。</span><span class="sxs-lookup"><span data-stu-id="f0b83-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="f0b83-119">このメソッドが現在のクエリ パラメーターを使用して、現在の**レコード セット**を再設定または引数 newquerydef で (Microsoft Access ワークスペース) で新しいファイルが提供されます。</span><span class="sxs-lookup"><span data-stu-id="f0b83-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="f0b83-120">Newquerydef 引数を省略する場合、最初の**レコード セット**を作成するために使用するパラメーターと同じクエリ定義に基づく**レコード セット**が再設定されます。</span><span class="sxs-lookup"><span data-stu-id="f0b83-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="f0b83-121">基になるデータに変更があった場合は、この再読み込み時に反映されます。</span><span class="sxs-lookup"><span data-stu-id="f0b83-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="f0b83-122">**QueryDef** を使用して **Recordset** を作成していない場合は、 **Recordset** が最初から再作成されます。</span><span class="sxs-lookup"><span data-stu-id="f0b83-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="f0b83-123">Newquerydef 引数に元の**クエリ定義**を指定する場合、**レコード セット**に対してクエリが実行**クエリ定義**で指定されたパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="f0b83-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="f0b83-124">基になるデータに変更があった場合は、この再読み込み時に反映されます。</span><span class="sxs-lookup"><span data-stu-id="f0b83-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="f0b83-125">**レコード セット**内のクエリ パラメーター値への変更を反映するためには、引数 newquerydef を指定してください。</span><span class="sxs-lookup"><span data-stu-id="f0b83-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="f0b83-126">最初に **Recordset** を作成したときとは異なる **QueryDef** を指定した場合、 **Recordset** は最初から再作成されます。</span><span class="sxs-lookup"><span data-stu-id="f0b83-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="f0b83-127">**Requery** を使用すると、 **Recordset** 内の最初のレコードがカレント レコードとなります。</span><span class="sxs-lookup"><span data-stu-id="f0b83-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="f0b83-128">**Requery** メソッドは、 [**Restartable**](recordset2-restartable-property-dao.md) プロパティが **False** に設定されているダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="f0b83-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="f0b83-129">Newquerydef の省略可能な引数を指定する場合は、 **Restartable**プロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f0b83-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="f0b83-130">[Requery](recordset2-bof-property-dao.md) を使用した後に、 **Recordset** オブジェクトの **[BOF](recordset2-eof-property-dao.md)** プロパティと \*\*\*\*EOF\*\*\*\* プロパティの両方の設定が **True** になった場合、クエリによってレコードは返されておらず、 **Recordset** にはデータが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f0b83-130">If both the **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="f0b83-131">例</span><span class="sxs-lookup"><span data-stu-id="f0b83-131">Example</span></span>

<span data-ttu-id="f0b83-132">この例では、 **Requery** メソッドを使用して、基になるデータが変更された後にクエリを更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f0b83-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="f0b83-133">この例では、 **Requery** メソッドを使用して、クエリ パラメーターが変更された後にクエリを更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f0b83-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```
