---
title: Field2.Required プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6b1950c8a864fbf23bee26be89e07e49357840b7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709048"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="2c1bc-102">Field2.Required プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="2c1bc-102">Field2.Required property (DAO)</span></span>


<span data-ttu-id="2c1bc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="2c1bc-104">**Field2** オブジェクトに非 Null 値が必須かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1bc-105">構文</span><span class="sxs-lookup"><span data-stu-id="2c1bc-105">Syntax</span></span>

<span data-ttu-id="2c1bc-106">*式*です。必須</span><span class="sxs-lookup"><span data-stu-id="2c1bc-106">*expression* .Required</span></span>

<span data-ttu-id="2c1bc-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c1bc-108">注釈</span><span class="sxs-lookup"><span data-stu-id="2c1bc-108">Remarks</span></span>

<span data-ttu-id="2c1bc-109">**Fields** コレクションに追加されていない **Field2** オブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="2c1bc-110">**Required** プロパティを使用できるかどうかは、次の表に示すように、 **[Fields](fields-collection-dao.md)** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c1bc-111">Fields コレクションが属するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="2c1bc-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="2c1bc-112">Required プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="2c1bc-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c1bc-113"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2c1bc-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2c1bc-114">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c1bc-115"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2c1bc-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2c1bc-116">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="2c1bc-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c1bc-117"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2c1bc-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2c1bc-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="2c1bc-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c1bc-119"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2c1bc-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2c1bc-120">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c1bc-121"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2c1bc-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2c1bc-122">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c1bc-p101">**AllowZeroLength**、 **ValidateOnSet**、または **ValidationRule** の各プロパティに **Required** プロパティを使用すると、その **Field2** オブジェクトの **Value** プロパティの設定値の妥当性を調べることができます。 **Required** プロパティが **False** に設定されている場合、フィールドには **null** 値、および **AllowZeroLength** プロパティと **ValidationRule** プロパティの設定値で指定された条件を満たす値を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="2c1bc-p102">[!メモ] **Index** オブジェクトと **Field2** オブジェクトのいずれかにこのプロパティを設定できる場合、 **Field2** オブジェクトのプロパティを設定します。 **Field2** オブジェクトのプロパティ設定の妥当性は、 **Index** オブジェクトのプロパティ設定よりも前に確認されます。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-p102">When you can set this property for either an **Index** object or a **Field2** object, set it for the **Field2** object. The validity of the property setting for a **Field2** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="2c1bc-127">例</span><span class="sxs-lookup"><span data-stu-id="2c1bc-127">Example</span></span>

<span data-ttu-id="2c1bc-p103">次の使用例は、 **Required** プロパティを使用して、新しいレコードを追加するためにデータを含める必要がある、3 つの異なるテーブルのフィールドをレポート出力します。このプロシージャを実行するには、RequiredOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="2c1bc-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

