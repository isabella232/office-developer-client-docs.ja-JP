---
title: Bookmarkable プロパティ (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 9c93d04d-ca10-acf5-122a-58625ed93424
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198125(v=office.15)
ms:contentKeyID: 48546601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052888
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 26b8b60255b4e50a2288dedb8e27906476926e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307456"
---
# <a name="recordset2bookmarkable-property-dao"></a>Bookmarkable プロパティ (DAO)


**適用先:** Access 2013、Office 2013

**Recordset** オブジェクトがブックマークをサポートし、 **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを使用してブックマークを設定できるかどうかを示す値を取得します。

## <a name="syntax"></a>構文

*式*。Bookmarkable

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Bookmark** プロパティを設定または確認しようとする前に、 **Recordset** オブジェクトの **Bookmarkable** プロパティの設定を確認してください。

Microsoft access データベースエンジンのテーブルを基にした**Recordset**オブジェクトの場合、 **Bookmarkable**プロパティの値は True になり、ブックマークを使用することができます。 ただし、他のデータベース製品はブックマークをサポートしていない場合があります。 たとえば、主キーを持たないリンク テーブルの Paradox に準拠する **Recordset** オブジェクトではブックマークを使用できません。

## <a name="example"></a>例

この例では、 **Bookmark** プロパティおよび **Bookmarkable** プロパティを使用して、ユーザーがレコードセット内のレコードにフラグを設定し、後でそのレコードに戻ることができるようにします。

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
