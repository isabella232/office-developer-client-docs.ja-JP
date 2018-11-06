---
title: Recordset2.NoMatch プロパティ (DAO)
TOCTitle: NoMatch Property
ms:assetid: 2d7a02ff-a2bf-5f0e-bd71-a6d42c25b13a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192114(v=office.15)
ms:contentKeyID: 48543972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6975a438e4e724a6fc1f72be92088f0d07a5b44
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996707"
---
# <a name="recordset2nomatch-property-dao"></a>Recordset2.NoMatch プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

**[Seek](recordset2-seek-method-dao.md)** メソッドを使用するかまたは **[Find](recordset2-findfirst-method-dao.md)** メソッドの 1 つを使用して、特定のレコードが見つかったかどうかを示します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。NoMatch

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**[Recordset](recordset-object-dao.md)** オブジェクトを開くかまたは作成すると、そのオブジェクトの **NoMatch** プロパティは **False** に設定されます。

レコードを見つける場合、テーブル タイプの **Recordset** オブジェクトに対しては **Seek** メソッドを使用し、ダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトに対しては **Find** メソッドのいずれか 1 つを使用します。 **NoMatch** プロパティの設定値を調べ、レコードが見つかったかどうかを確認します。

**Seek** メソッドまたは **Find** メソッドで検出されず、 **NoMatch** プロパティが **True** に設定されると、カレント レコードは無効になります。そのレコードに戻る必要がある場合は、 **Seek** メソッドまたは **Find** メソッドを使用する前に、カレント レコードのブックマークを取得してください。

> [!NOTE]
> [!メモ] [Recordset](recordset-movefirst-method-dao.md) オブジェクトでいずれの ****Move**** メソッドを使用しても、そのオブジェクトの **NoMatch** プロパティの設定値には反映されません。

## <a name="example"></a>例

次の例では、 **NoMatch** プロパティを使用して **Seek** および **FindFirst** が成功したかどうか確認し、成功しなかった場合は適切なフィードバックを表示します。このプロシージャを実行するには、SeekMatch プロシージャと FindMatch プロシージャが必要です。

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset2, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
