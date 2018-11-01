---
title: Recordset2.Bookmark プロパティ (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5336c0993230b7d380b335e6f8e7eaa1af9b306c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867826"
---
# <a name="recordset2bookmark-property-dao"></a><span data-ttu-id="0f708-102">Recordset2.Bookmark プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="0f708-102">Recordset2.Bookmark Property (DAO)</span></span>


<span data-ttu-id="0f708-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0f708-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f708-104">**Recordset** オブジェクト内のカレント レコードを一意に識別するブックマークを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="0f708-104">Sets or returns a bookmark that uniquely identifies the current record in a **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f708-105">構文</span><span class="sxs-lookup"><span data-stu-id="0f708-105">Syntax</span></span>

<span data-ttu-id="0f708-106">*式*です。ブックマーク</span><span class="sxs-lookup"><span data-stu-id="0f708-106">*expression* .Bookmark</span></span>

<span data-ttu-id="0f708-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="0f708-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f708-108">備考</span><span class="sxs-lookup"><span data-stu-id="0f708-108">Remarks</span></span>

<span data-ttu-id="0f708-109">**レコード セット**オブジェクトを Microsoft Access データベース エンジンのテーブルを基に、 **Bookmarkable**プロパティの値は、true の場合、およびそのレコード セットの**Bookmark**プロパティを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0f708-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use the **Bookmark** property with that recordset.</span></span> <span data-ttu-id="0f708-110">ただし、他のデータベース製品はブックマークをサポートしていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="0f708-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="0f708-111">たとえば、主キーを持たないリンク テーブルの Paradox に準拠する **Recordset2** オブジェクトではブックマークを使用できません。</span><span class="sxs-lookup"><span data-stu-id="0f708-111">For example, you can't use bookmarks in any **Recordset2** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="0f708-p102">**Recordset** オブジェクトを作成するか開くと、その各レコードは既に一意のブックマークを持っています。 **Bookmark** プロパティの値を変数に代入することにより、カレント レコードのブックマークを保存できます。別のレコードに移動した後、 **Recordset** オブジェクトの **Bookmark** プロパティをその変数の値に設定すると、いつでもそのレコードに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="0f708-p102">When you create or open a **Recordset** object, each of its records already has a unique bookmark. You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="0f708-p103">作成できるブックマークの数に制限はありません。カレント レコード以外のレコードのブックマークを作成するには、目的のレコードに移動してから、そのレコードを識別する文字列型 ( **String** ) の変数に **Bookmark** プロパティの値を代入します。</span><span class="sxs-lookup"><span data-stu-id="0f708-p103">There is no limit to the number of bookmarks you can establish. To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="0f708-117">**Recordset** オブジェクトでブックマークがサポートされるかどうかを確認するには、 [Bookmark](recordset2-bookmarkable-property-dao.md) プロパティを使用する前に、 \*\*\*\*Bookmarkable\*\*\*\* プロパティの値を調べます。</span><span class="sxs-lookup"><span data-stu-id="0f708-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="0f708-118">**Bookmarkable**プロパティが False の場合は、 **Recordset**オブジェクトがブックマークをサポートしていませんし、**ブックマーク**を使用してプロパティをトラップ可能なエラーの結果です。</span><span class="sxs-lookup"><span data-stu-id="0f708-118">If the **Bookmarkable** property is False, the **Recordset** object doesn't support bookmarks, and using the **Bookmark** property results in a trappable error.</span></span>

<span data-ttu-id="0f708-p105">**[Clone](recordset2-clone-method-dao.md)** メソッドを使用して **Recordset** オブジェクトのコピーを作成した場合、複製元および複製された **Recordset** オブジェクトの **Bookmark** プロパティの設定は同一になり、相互に使用することができます。一方、異なる **Recordset** オブジェクトのブックマークは、たとえ同一のオブジェクトまたは同一の SQL ステートメントを使用して作成したものであっても、相互に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="0f708-p105">If you use the **[Clone](recordset2-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably. However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="0f708-121">**Bookmark** プロパティを削除済みレコードを表す値に設定すると、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0f708-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="0f708-122">**Bookmark** プロパティの値は、レコード番号と同一ではありません。</span><span class="sxs-lookup"><span data-stu-id="0f708-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="0f708-123">例</span><span class="sxs-lookup"><span data-stu-id="0f708-123">Example</span></span>

<span data-ttu-id="0f708-124">この例では、 **Bookmark** プロパティおよび **Bookmarkable** プロパティを使用して、ユーザーがレコードセット内のレコードにフラグを設定し、後でそのレコードに戻ることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="0f708-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="0f708-125">この例では、 **LastModified** プロパティを使用して、カレント レコードを参照するポインターを、変更したレコードおよび新しく作成したレコードの両方に移動します。</span><span class="sxs-lookup"><span data-stu-id="0f708-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
