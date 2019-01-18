---
title: Recordset.AbsolutePosition プロパティ (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 22284abf537f57d98d5f0416b58a9a2ac3c6ebe5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702505"
---
# <a name="recordsetabsoluteposition-property-dao"></a><span data-ttu-id="a3d6e-102">Recordset.AbsolutePosition プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3d6e-102">Recordset.AbsolutePosition property (DAO)</span></span>

<span data-ttu-id="a3d6e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3d6e-104">**Recordset** オブジェクトのカレント レコードの相対的なレコード番号を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-104">Sets or returns the relative record number of a **Recordset** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d6e-105">構文</span><span class="sxs-lookup"><span data-stu-id="a3d6e-105">Syntax</span></span>

<span data-ttu-id="a3d6e-106">*式*です。AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="a3d6e-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="a3d6e-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d6e-108">注釈</span><span class="sxs-lookup"><span data-stu-id="a3d6e-108">Remarks</span></span>

<span data-ttu-id="a3d6e-p101">**AbsolutePosition** プロパティを使用すると、ダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクト内における順序位置に基づいて、カレント レコードを参照するポインターを特定のレコードに移動できます。また、 **AbsolutePosition** プロパティの設定値を調べると、カレント レコードのレコード番号を特定できます。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="a3d6e-p102">**AbsolutePosition** プロパティの値は 0 から始まるため (つまり、設定値 0 は **Recordset** オブジェクトの最初のレコードを表します)、このプロパティを、格納済みのレコードの数に等しいかまたはそれを超える値に設定できません。このような値に設定すると、トラップ可能なエラーが発生します。 **RecordCount** プロパティの設定値を調べると、 **Recordset** オブジェクトに格納済みのレコードの数を確認できます。 **AbsolutePosition** プロパティに設定できる最大の値は、 **RecordCount** プロパティから 1 を引いた値です。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="a3d6e-114">ない場合、現在のレコードとして**レコード セット**オブジェクトのレコードが存在しない場合、 **AbsolutePosition**は-1 を返します。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-114">If there is no current record, as when there are no records in the **Recordset** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="a3d6e-115">カレント レコードを削除した場合、 **AbsolutePosition** プロパティに値が定義されていないため、そのレコードを参照するとトラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="a3d6e-116">新しいレコードは、レコード順序の末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="a3d6e-p104">このプロパティをレコード番号の代わりに使用しないでください。ブックマークが、特定の位置を保持してその位置に戻るための推奨手段であり、すべての種類の **Recordset** オブジェクトでカレント レコードの位置を指定する唯一の手段です。特に、レコードの位置は、それより前にある 1 つ以上のレコードを削除すると変わります。また、SQL ステートメントで ORDER BY 句を使用して **Recordset** オブジェクトを作成した場合を除き、そのオブジェクト内の各レコードの順序は保証されないため、 **Recordset** オブジェクトを再作成すると、同じレコードの絶対的な位置が以前と同じになる保証はありません。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="a3d6e-p105">新たに開いた後でまだレコードを格納していない **Recordset** オブジェクトの **AbsolutePosition** プロパティを 0 より大きい値に設定すると、トラップ可能なエラーが発生します。**MoveLast** メソッドを使用して、まず **Recordset** オブジェクトに値を設定してください。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-p105">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset** object causes a trappable error. Populate the **Recordset** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="a3d6e-123">前方スクロール タイプの **Recordset** オブジェクト、または Microsoft Access データベース エンジンに接続された ODBC データベースに対して実行したパススルー クエリによって開いた **Recordset** オブジェクトでは、**AbsolutePosition** プロパティを使用できません。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset** objects, or on **Recordset** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="a3d6e-124">例</span><span class="sxs-lookup"><span data-stu-id="a3d6e-124">Example</span></span>

<span data-ttu-id="a3d6e-125">この例では、 **AbsolutePosition** プロパティを使用して、 **Recordset** オブジェクトのすべてのレコードを列挙するループ処理の進捗を追跡します。</span><span class="sxs-lookup"><span data-stu-id="a3d6e-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
