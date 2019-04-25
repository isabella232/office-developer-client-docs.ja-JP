---
title: Recordset.Bookmark プロパティ (DAO)
TOCTitle: Bookmark Property
ms:assetid: c4b1c2d9-668e-e365-544c-efb4ae4efcc9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823084(v=office.15)
ms:contentKeyID: 48547597
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052887
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1ebf963695b2d754a4501077e2236c52280a9a2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300652"
---
# <a name="recordsetbookmark-property-dao"></a><span data-ttu-id="29934-102">Recordset.Bookmark プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="29934-102">Recordset.Bookmark Property (DAO)</span></span>


<span data-ttu-id="29934-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="29934-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29934-104">**[Recordset](recordset-object-dao.md)** オブジェクトのカレント レコードを一意に識別するブックマークを設定または返します。</span><span class="sxs-lookup"><span data-stu-id="29934-104">Sets or returns a bookmark that uniquely identifies the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="29934-105">構文</span><span class="sxs-lookup"><span data-stu-id="29934-105">Syntax</span></span>

<span data-ttu-id="29934-106">*式* .Bookmark</span><span class="sxs-lookup"><span data-stu-id="29934-106">expression  . Bookmark</span></span>

<span data-ttu-id="29934-107">*式* **Recordset** オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="29934-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="29934-108">注釈</span><span class="sxs-lookup"><span data-stu-id="29934-108">Remarks</span></span>

<span data-ttu-id="29934-109">Microsoft Access データベース エンジンのテーブルに完全に準拠した **Recordset** オブジェクトでは、**Bookmarkable** プロパティの値は True に設定され、その **Recordset**で**Bookmark**プロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="29934-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is  **True**, and you can use the **Bookmark** property with that recordset.</span></span> <span data-ttu-id="29934-110">ただし、他のデータベース製品はブックマークをサポートしていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="29934-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="29934-111">たとえば、主キーを持たないリンク テーブルの Paradox に準拠する **Recordset** オブジェクトではブックマークを使用できません。</span><span class="sxs-lookup"><span data-stu-id="29934-111">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="29934-p102">
            \*\*Recordset\*\* オブジェクトを作成するか開くと、その各レコードは既に一意のブックマークを持っています。\*\*Bookmark\*\* プロパティの値を変数に代入することにより、カレント レコードのブックマークを保存できます。別のレコードに移動した後、\*\*Recordset\*\* オブジェクトの \*\*Bookmark\*\* プロパティをその変数の値に設定すると、いつでもそのレコードに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="29934-p102">When you create or open a **Recordset** object, each of its records already has a unique bookmark. You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="29934-p103">作成できるブックマークの数に制限はありません。カレント レコード以外のレコードのブックマークを作成するには、目的のレコードに移動してから、そのレコードを識別する文字列型 (**String**) の変数に **Bookmark** プロパティの値を代入します。</span><span class="sxs-lookup"><span data-stu-id="29934-p103">There is no limit to the number of bookmarks you can establish. To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="29934-117">**Recordset** オブジェクトは、ブックマークをサポートするか確認するためには、**Bookmark** プロパティを使用する前に、**[Bookmarkable](recordset-bookmarkable-property-dao.md)** プロパティの値をチェックします。</span><span class="sxs-lookup"><span data-stu-id="29934-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="29934-118">**Bookmarkable**プロパティが False の場合、**Recordset** オブジェクトはブックマークをサポートしていないため、**Bookmark** プロパティを使用するとトラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="29934-118">If the Bookmarkable property is False, the Recordset object doesn't support bookmarks, and using the Bookmark property results in a trappable error.</span></span>

<span data-ttu-id="29934-p105">
            **
            [Clone](recordset-clone-method-dao.md)*\* メソッドを使用して \*\*Recordset\*\* オブジェクトのコピーを作成した場合、複製元および複製された \*\*Recordset\*\* オブジェクトの \*\*Bookmark\*\* プロパティの設定は同一になり、相互に使用することができます。一方、異なる \*\*Recordset\*\* オブジェクトのブックマークは、たとえ同一のオブジェクトまたは同一の SQL ステートメントを使用して作成したものであっても、相互に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="29934-p105">If you use the **[Clone](recordset-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably. However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="29934-121">
            \*\*Bookmark\*\* プロパティを削除済みレコードを表す値に設定すると、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="29934-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="29934-122">
            \*\*Bookmark\*\* プロパティの値は、レコード番号と同一ではありません。</span><span class="sxs-lookup"><span data-stu-id="29934-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="29934-123">例</span><span class="sxs-lookup"><span data-stu-id="29934-123">Example</span></span>

<span data-ttu-id="29934-124">この例では、**Bookmark** プロパティおよび **Bookmarkable** プロパティを使用して、ユーザーが **Recordset** 内のレコードにフラグを設定し、後でそのレコードに戻ることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="29934-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
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

<span data-ttu-id="29934-125">この例では、**LastModified** プロパティを使用して、カレント レコードを参照するポインターを、変更したレコードおよび新しく作成したレコードの両方に移動します。</span><span class="sxs-lookup"><span data-stu-id="29934-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
