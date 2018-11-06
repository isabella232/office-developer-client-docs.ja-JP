---
title: Recordset2.PercentPosition プロパティ (DAO)
TOCTitle: PercentPosition Property
ms:assetid: 830a7d26-6817-233f-ce24-80b572c1c100
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196732(v=office.15)
ms:contentKeyID: 48545996
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052973
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7cf5a0e0a9d0cf3d3cd5ce2b89dc287b41c72f74
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998798"
---
# <a name="recordset2percentposition-property-dao"></a><span data-ttu-id="83674-102">Recordset2.PercentPosition プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="83674-102">Recordset2.PercentPosition property (DAO)</span></span>

<span data-ttu-id="83674-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="83674-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83674-104">**[Recordset](recordset-object-dao.md)** オブジェクト内のレコード数の割合に基づいて、 **Recordset** オブジェクトのカレント レコードのおよその位置を示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="83674-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="83674-105">構文</span><span class="sxs-lookup"><span data-stu-id="83674-105">Syntax</span></span>

<span data-ttu-id="83674-106">*式*です。PercentPosition</span><span class="sxs-lookup"><span data-stu-id="83674-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="83674-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="83674-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="83674-108">注釈</span><span class="sxs-lookup"><span data-stu-id="83674-108">Remarks</span></span>

<span data-ttu-id="83674-p101">**Recordset** オブジェクト内のカレント レコードのおよその位置を示したり変更したりするには、 **PercentPosition** プロパティを確認または設定します。ベース テーブルから直接開いたダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトを使用する場合は、 **PercentPosition** プロパティを設定または確認する前に、最後のレコードに移動して **Recordset** オブジェクトに値を設定します。 **Recordset** オブジェクトに値がすべて設定される前に **PercentPosition** プロパティを使用すると、移動量は、 **[RecordCount](recordset2-recordcount-property-dao.md)** プロパティの設定値に示されている、アクセス済みのレコード数に対する割合になります。 **[MoveLast](recordset2-movelast-method-dao.md)** メソッドを使用すると、最後のレコードに移動できます。</span><span class="sxs-lookup"><span data-stu-id="83674-p101">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property. When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property. If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset2-recordcount-property-dao.md)** property setting. You can move to the last record by using the **[MoveLast](recordset2-movelast-method-dao.md)** method.</span></span>

> [!NOTE]
> <span data-ttu-id="83674-113">**PercentPosition**プロパティを使用して、**レコード セット**オブジェクトの特定のレコードをカレント レコードを移動するのにはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="83674-113">Using the **PercentPosition** property to move the current record to a specific record in a **Recordset** object isn't recommended.</span></span> <span data-ttu-id="83674-114">**[Bookmark](recordset2-bookmark-property-dao.md)** プロパティは、この作業に適しています。</span><span class="sxs-lookup"><span data-stu-id="83674-114">The **[Bookmark](recordset2-bookmark-property-dao.md)** property is better suited for this task.</span></span>

<span data-ttu-id="83674-p103">いったん **PercentPosition** プロパティをある値に設定すると、その値に対応するおよその位置にあるレコードがカレント レコードになり、 **PercentPosition** プロパティはカレント レコードのおよその位置が反映された値に再設定されます。たとえば、 **Recordset** オブジェクトに格納されているレコードが 5 件のみの場合に、その **PercentPosition** プロパティの値を 77 に設定すると、 **PercentPosition** プロパティから取得される値は 77 ではなく 80 になることがあります。</span><span class="sxs-lookup"><span data-stu-id="83674-p103">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record. For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="83674-117">**PercentPosition**プロパティは、前方スクロール タイプの**Recordset**オブジェクト、またはリモート ・ データベースに対してパススルー クエリから**レコード セット**オブジェクトを除いて、**レコード セット**オブジェクトのすべての種類に適用されます。</span><span class="sxs-lookup"><span data-stu-id="83674-117">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="83674-118">フォームまたはテキスト ボックスのスクロール バーに **PercentPosition** プロパティを使用すると、 **Recordset** オブジェクト内のカレント レコードの位置を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="83674-118">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="83674-119">例</span><span class="sxs-lookup"><span data-stu-id="83674-119">Example</span></span>

<span data-ttu-id="83674-120">この例では、 **PercentPosition** プロパティを使用して、 **Recordset** オブジェクトの先頭を基準として、カレント レコードを参照するポインターの位置を示します。</span><span class="sxs-lookup"><span data-stu-id="83674-120">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
