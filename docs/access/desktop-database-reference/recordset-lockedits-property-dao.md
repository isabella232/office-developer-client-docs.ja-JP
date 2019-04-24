---
title: LockEdits プロパティ (DAO)
TOCTitle: LockEdits Property
ms:assetid: baa11b24-a330-eaa4-bd03-b8b9739d209e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822514(v=office.15)
ms:contentKeyID: 48547379
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052877
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 54f91dea98f4f47057eb673a0fae08c8ac2b6f1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300463"
---
# <a name="recordsetlockedits-property-dao"></a>LockEdits プロパティ (DAO)

**適用先:** Access 2013、Office 2013

編集時に有効になるロック状態の種類を示す値を設定または取得します。

## <a name="syntax"></a>構文

*式*。LockEdits

*式***Recordset**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

次の表は、この設定値または戻り値が表すロック状態の種類です。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>正しい</p></td>
<td><p>既定値です。排他的ロックが有効になります。Edit メソッドを呼び出した直後に、編集中のレコードが含まれているページがロックされます。</p></td>
</tr>
<tr class="even">
<td><p>誤り</p></td>
<td><p>編集に対して共有的ロックが有効になります。 Update メソッドが実行されるまで、record を含むページはロックされません。</p></td>
</tr>
</tbody>
</table>


**LockEdits** プロパティは、更新可能な **[Recordset](recordset-object-dao.md)** オブジェクトで使用できます。

ページがロックされている場合、他のユーザーは同じページのレコードを編集できません。 **LockEdits** プロパティを **True** に設定した場合、 **Edit** メソッドを使用するときに別のユーザーが既にページをロックしていると、エラーが発生します。他のユーザーは、ロックされているページからデータを読み取ることができます。

**LockEdits** プロパティを **False** に設定した場合は、別のユーザーがページをロックしているときに **Update** メソッドを使用すると、エラーが発生します。使用中のレコードに対して別のユーザーが行った変更の内容を表示するには、引数を 0 に設定して **[Move](recordset-move-method-dao.md)** メソッドを使用します。ただし、このメソッドを実行すると、それまでに行った変更の内容が失われます。

Microsoft Access データベース エンジンに接続された ODBC データ ソースを使用する場合は、 **LockEdits** プロパティを常に **False** に設定するか、または共有的ロックを有効にします。Microsoft Access データベース エンジンは、外部のデータベース サーバーで使用されるロック機能に対する制御は行いません。

> [!NOTE]
> **[OpenRecordset](connection-openrecordset-method-dao.md)** メソッドの引数 lockedits を事前に設定しておくと、初めて **Recordset** オブジェクトを開くときに **LockEdits** プロパティの値を設定できます。 引数 lockedits を **dbPessimistic** に設定すると **LockEdits** プロパティが **True** に設定され、lockedits をそれ以外の値に設定すると **LockEdits** プロパティが **False** に設定されます。

## <a name="example"></a>例

この例は、まず **LockEdits** プロパティを **True** に設定して排他的ロックを有効にする方法を示し、次に **LockEdits** プロパティを False に設定して共有的ロックを有効にする方法を示します。また、マルチユーザー データベースの環境でフィールドを変更するために必要なエラー処理の種類を示します。このプロシージャを実行するには、PessimisticLock 関数および OptimisticLock 関数が必要です。

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
