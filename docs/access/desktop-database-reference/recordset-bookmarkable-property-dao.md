---
title: Recordset.Bookmarkable プロパティ (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8eca86433098256128dc78cb1c2cf6fd8b87ec6c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889197"
---
# <a name="recordsetbookmarkable-property-dao"></a>Recordset.Bookmarkable プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

**Recordset** オブジェクトがブックマークをサポートしているかどうかを示す、 **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを使用して設定できる値を返します。

## <a name="syntax"></a>構文

*式*です。ブックマークを設定

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Bookmark** プロパティを設定または確認しようとする前に、 **Recordset** オブジェクトの **Bookmarkable** プロパティの設定値を確認してください。

Microsoft Access データベース エンジンのテーブルに基づく**Recordset**オブジェクトの**Bookmarkable**プロパティの値は、true の場合、およびブックマークを使用することができます。 ただし、その他のデータベース製品では、ブックマークがサポートされていない場合があります。 たとえば、主キーがない Paradox リンク テーブルを基にした **Recordset** オブジェクトでブックマークを使用することはできません。

## <a name="example"></a>例

次の使用例は、 **Bookmark** プロパティと **Bookmarkable** プロパティを使用して、後からそのレコードに戻れるように、ユーザーが **Recordset** オブジェクトのレコードにフラグを立てることができるようにします。

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
