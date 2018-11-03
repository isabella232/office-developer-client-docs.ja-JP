---
title: Field2.Required プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf5e459773cd0fa0976704834b1b73467fc75294
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937408"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="8e339-102">Field2.Required プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e339-102">Field2.Required property (DAO)</span></span>


<span data-ttu-id="8e339-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8e339-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8e339-104">**Field2** オブジェクトに非 Null 値が必須かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="8e339-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e339-105">構文</span><span class="sxs-lookup"><span data-stu-id="8e339-105">Syntax</span></span>

<span data-ttu-id="8e339-106">*式*です。必須</span><span class="sxs-lookup"><span data-stu-id="8e339-106">*expression* .Required</span></span>

<span data-ttu-id="8e339-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="8e339-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e339-108">注釈</span><span class="sxs-lookup"><span data-stu-id="8e339-108">Remarks</span></span>

<span data-ttu-id="8e339-109">**Fields** コレクションに追加されていない **Field2** オブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="8e339-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="8e339-110">**Required** プロパティを使用できるかどうかは、次の表に示すように、 **[Fields](fields-collection-dao.md)** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="8e339-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e339-111">Fields コレクションが属するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="8e339-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="8e339-112">Required プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="8e339-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e339-113"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8e339-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e339-114">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="8e339-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e339-115"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8e339-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e339-116">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="8e339-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e339-117"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8e339-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e339-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="8e339-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e339-119"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8e339-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e339-120">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="8e339-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e339-121"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8e339-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e339-122">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="8e339-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8e339-p101">**AllowZeroLength**、 **ValidateOnSet**、または **ValidationRule** の各プロパティに **Required** プロパティを使用すると、その **Field2** オブジェクトの **Value** プロパティの設定値の妥当性を調べることができます。 **Required** プロパティが **False** に設定されている場合、フィールドには **null** 値、および **AllowZeroLength** プロパティと **ValidationRule** プロパティの設定値で指定された条件を満たす値を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8e339-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="8e339-p102">[!メモ] **Index** オブジェクトと **Field2** オブジェクトのいずれかにこのプロパティを設定できる場合、 **Field2** オブジェクトのプロパティを設定します。 **Field2** オブジェクトのプロパティ設定の妥当性は、 **Index** オブジェクトのプロパティ設定よりも前に確認されます。</span><span class="sxs-lookup"><span data-stu-id="8e339-p102">When you can set this property for either an **Index** object or a **Field2** object, set it for the **Field2** object. The validity of the property setting for a **Field2** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="8e339-127">例</span><span class="sxs-lookup"><span data-stu-id="8e339-127">Example</span></span>

<span data-ttu-id="8e339-p103">次の使用例は、 **Required** プロパティを使用して、新しいレコードを追加するためにデータを含める必要がある、3 つの異なるテーブルのフィールドをレポート出力します。このプロシージャを実行するには、RequiredOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="8e339-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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

