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
ms.openlocfilehash: c61cc86fbca68e8c3aca38fd86ed36b8c8f403dd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477680"
---
# <a name="recordsetbookmark-property-dao"></a>Recordset.Bookmark プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトのカレント レコードを一意に識別するブックマークを設定または取得します。

## <a name="syntax"></a>構文

*式*です。ブックマーク

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>備考

**レコード セット**オブジェクトを Microsoft Access データベース エンジンのテーブルを基に、 **Bookmarkable**プロパティの値は、true の場合、およびその**レコード セット**の**Bookmark**プロパティを使用することができます。 ただし、その他のデータベース製品では、ブックマークがサポートされていない場合があります。 たとえば、主キーを持たないリンク テーブルの Paradox に準拠する **Recordset** オブジェクトではブックマークを使用できません。

**Recordset** オブジェクトを作成するか開くと、その各レコードは既に一意のブックマークを持っています。 **Bookmark** プロパティの値を変数に代入することにより、カレント レコードのブックマークを保存できます。別のレコードに移動した後、 **Recordset** オブジェクトの **Bookmark** プロパティをその変数の値に設定すると、いつでもそのレコードに戻ることができます。

作成できるブックマークの数に制限はありません。カレント レコード以外のレコードのブックマークを作成するには、目的のレコードに移動してから、そのレコードを識別する文字列型 ( **String** ) の変数に **Bookmark** プロパティの値を代入します。

**Recordset** オブジェクトでブックマークがサポートされるかどうかを確認するには、 [Bookmark](recordset-bookmarkable-property-dao.md) プロパティを使用する前に、 ****Bookmarkable**** プロパティの値を調べます。 **Bookmarkable**プロパティが False の場合は、 **Recordset**オブジェクトがブックマークをサポートしていませんし、**ブックマーク**を使用してプロパティをトラップ可能なエラーの結果です。

**[Clone](recordset-clone-method-dao.md)** メソッドを使用して **Recordset** オブジェクトのコピーを作成した場合、複製元および複製された **Recordset** オブジェクトの **Bookmark** プロパティの設定は同一になり、相互に使用することができます。一方、異なる **Recordset** オブジェクトのブックマークは、たとえ同一のオブジェクトまたは同一の SQL ステートメントを使用して作成したものであっても、相互に使用することはできません。

**Bookmark** プロパティを削除済みレコードを表す値に設定すると、トラップ可能なエラーが発生します。

**Bookmark** プロパティの値は、レコード番号と同一ではありません。

## <a name="example"></a>例

この例では、 **Bookmark** プロパティおよび **Bookmarkable** プロパティを使用して、ユーザーが **Recordset** 内のレコードにフラグを設定し、後でそのレコードに戻ることができるようにします。

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

この例では、 **LastModified** プロパティを使用して、カレント レコードを参照するポインターを、変更したレコードおよび新しく作成したレコードの両方に移動します。

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
