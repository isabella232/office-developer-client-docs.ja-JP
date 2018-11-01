---
title: Field2.Required プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e6d4963ed10f2bf886a7445dfa05f1a3fcef460
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872943"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="6d2af-102">Field2.Required プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d2af-102">Field2.Required Property (DAO)</span></span>


<span data-ttu-id="6d2af-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6d2af-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6d2af-104">**Field2** オブジェクトに非 Null 値が必須かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="6d2af-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2af-105">構文</span><span class="sxs-lookup"><span data-stu-id="6d2af-105">Syntax</span></span>

<span data-ttu-id="6d2af-106">*式*です。必須</span><span class="sxs-lookup"><span data-stu-id="6d2af-106">*expression* .Required</span></span>

<span data-ttu-id="6d2af-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6d2af-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d2af-108">注釈</span><span class="sxs-lookup"><span data-stu-id="6d2af-108">Remarks</span></span>

<span data-ttu-id="6d2af-109">**Fields** コレクションに追加されていない **Field2** オブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="6d2af-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="6d2af-110">**Required** プロパティを使用できるかどうかは、次の表に示すように、 **[Fields](fields-collection-dao.md)** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="6d2af-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d2af-111">Fields コレクションが属するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="6d2af-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="6d2af-112">Required プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="6d2af-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d2af-113"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6d2af-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6d2af-114">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="6d2af-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d2af-115"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6d2af-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6d2af-116">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6d2af-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d2af-117"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6d2af-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6d2af-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6d2af-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d2af-119"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6d2af-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6d2af-120">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="6d2af-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d2af-121"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6d2af-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="6d2af-122">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="6d2af-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6d2af-p101">**AllowZeroLength**、 **ValidateOnSet**、または **ValidationRule** の各プロパティに **Required** プロパティを使用すると、その **Field2** オブジェクトの **Value** プロパティの設定値の妥当性を調べることができます。 **Required** プロパティが **False** に設定されている場合、フィールドには **null** 値、および **AllowZeroLength** プロパティと **ValidationRule** プロパティの設定値で指定された条件を満たす値を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6d2af-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6d2af-p102">[!メモ] <STRONG>Index</STRONG> オブジェクトと <STRONG>Field2</STRONG> オブジェクトのいずれかにこのプロパティを設定できる場合、 <STRONG>Field2</STRONG> オブジェクトのプロパティを設定します。 <STRONG>Field2</STRONG> オブジェクトのプロパティ設定の妥当性は、 <STRONG>Index</STRONG> オブジェクトのプロパティ設定よりも前に確認されます。</span><span class="sxs-lookup"><span data-stu-id="6d2af-p102">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field2</STRONG> object, set it for the <STRONG>Field2</STRONG> object. The validity of the property setting for a <STRONG>Field2</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



## <a name="example"></a><span data-ttu-id="6d2af-127">例</span><span class="sxs-lookup"><span data-stu-id="6d2af-127">Example</span></span>

<span data-ttu-id="6d2af-p103">次の使用例は、 **Required** プロパティを使用して、新しいレコードを追加するためにデータを含める必要がある、3 つの異なるテーブルのフィールドをレポート出力します。このプロシージャを実行するには、RequiredOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="6d2af-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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

