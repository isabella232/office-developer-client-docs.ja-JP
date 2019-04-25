---
title: Recordset.Requery メソッド (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: bd6f2fdf7d1f8ba9fc47c6223a8f872a655a1e3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307624"
---
# <a name="recordsetrequery-method-dao"></a><span data-ttu-id="7dc1f-102">Recordset.Requery メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="7dc1f-102">Recordset.Requery Method (DAO)</span></span>

<span data-ttu-id="7dc1f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dc1f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7dc1f-104">**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行して、そのオブジェクトのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc1f-105">構文</span><span class="sxs-lookup"><span data-stu-id="7dc1f-105">Syntax</span></span>

<span data-ttu-id="7dc1f-106">*式* .Requery(***NewQueryDef***)</span><span class="sxs-lookup"><span data-stu-id="7dc1f-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="7dc1f-107">*式* **Recordset** オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dc1f-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7dc1f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7dc1f-109">名前</span><span class="sxs-lookup"><span data-stu-id="7dc1f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7dc1f-110">必須 / オプション </span><span class="sxs-lookup"><span data-stu-id="7dc1f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7dc1f-111">データ型</span><span class="sxs-lookup"><span data-stu-id="7dc1f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7dc1f-112">説明</span><span class="sxs-lookup"><span data-stu-id="7dc1f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7dc1f-113"><em>NewQueryDef</em></span><span class="sxs-lookup"><span data-stu-id="7dc1f-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="7dc1f-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="7dc1f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="7dc1f-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7dc1f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7dc1f-116"><strong>
            <a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトの <strong>Name</strong> プロパティの値を表します。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7dc1f-117">注釈</span><span class="sxs-lookup"><span data-stu-id="7dc1f-117">Remarks</span></span>

<span data-ttu-id="7dc1f-118">**Recordset** が最新のデータを含んでいるかこの方法を使って確認します。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="7dc1f-119">このメソッドでは、現在のクエリ パラメーターを使用するか、または (Microsoft Access ワークスペースの場合)、newquerydef 引数で指定された新しいクエリ を使用して、現在の**Recordset**にデータが再読み込みされます。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the  newquerydef argument.</span></span>

<span data-ttu-id="7dc1f-120">newquerydef 引数を指定しない場合、 **Recordset** に対するデータの再読み込みは、その **Recordset** に最初にデータが読み込まれたときと同じクエリ定義とパラメーターに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-120">If you don't specify a  newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="7dc1f-121">基になるデータに変更があった場合は、この再読み込み時に反映されます。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="7dc1f-122">**QueryDef** を使用して **Recordset** を作成していない場合は、 **Recordset** が最初から再作成されます。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="7dc1f-123">newquerydef 引数に元の **QueryDef**を指定した場合は、**QueryDef** で指定されたパラメーターを使用して **Recordset** が再取得されます。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-123">If you specify the original **QueryDef** in the  newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="7dc1f-124">この再読み込み中に、基になるデータの変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="7dc1f-125">クエリ パラメーターの値に対する変更を **Recordset** に反映するには、newquerydef 引数を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the  newquerydef argument.</span></span>

<span data-ttu-id="7dc1f-126">最初に **Recordset** を作成したときとは異なる **QueryDef** を指定した場合、**Recordset** は最初から再作成されます。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="7dc1f-127">
            \*\*Requery\*\* を使用すると、\*\*Recordset\*\* 内の最初のレコードがカレント レコードとなります。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="7dc1f-128">**Requery** メソッドは、 [**Restartable**](recordset-restartable-property-dao.md) プロパティが **False** に設定されているダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="7dc1f-129">しかし、オプションの newquerydef 引数を指定した場合は、 **Restartable** プロパティが無視されます。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-129">However, if you supply the optional  newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="7dc1f-130">**Requery**メソッドを使用した後に、**Recordset**オブジェクトの**[BOF](recordset-bof-property-dao.md)** と**[EOF](recordset-eof-property-dao.md)** プロパティの両方の設定が**True** になった場合、クエリはレコードを返さず、**Recordset**にデータは含まれません。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-130">If both the [**BOF**](recordset-bof-property-dao.md) and [**EOF**](recordset-eof-property-dao.md) property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="7dc1f-131">例</span><span class="sxs-lookup"><span data-stu-id="7dc1f-131">Example</span></span>

<span data-ttu-id="7dc1f-132">この例では、**Requery** メソッドを使用して、基になるデータが変更された後にクエリを更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
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

<span data-ttu-id="7dc1f-133">この例では、**Requery** メソッドを使用して、クエリ パラメーターが変更された後にクエリを更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7dc1f-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
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

