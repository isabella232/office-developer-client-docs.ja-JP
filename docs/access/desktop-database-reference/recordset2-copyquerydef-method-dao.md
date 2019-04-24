---
title: Recordset2 の copyquerydef メソッド (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: 36689ac0-f8a6-1f3e-4170-799141373777
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192474(v=office.15)
ms:contentKeyID: 48544170
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053073
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8a643dae0b67cf4f2a2a0148619d9a8f4df7e6f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307365"
---
# <a name="recordset2copyquerydef-method-dao"></a>Recordset2 の copyquerydef メソッド (DAO)


**適用先:** Access 2013、Office 2013 

recordset の**[](querydef-object-dao.md)** プレースホルダーで表される**[recordset](recordset-object-dao.md)** オブジェクトの作成**** に使用される querydef オブジェクトを返します (Microsoft Access ワークスペースのみ)。 .

## <a name="syntax"></a>構文

*式*。CopyQueryDef

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="return-value"></a>戻り値

QueryDef

## <a name="remarks"></a>注釈

**CopyQueryDef** メソッドを使用すると、 **Recordset** の作成に使用された **QueryDef** の複製である新しい **QueryDef** を作成できます。

**QueryDef** を使用してこの **Recordset** が作成されていない場合は、エラーが発生します。 **CopyQueryDef** メソッドを使用する前に、まず **OpenRecordset** メソッドを使用して **Recordset** を開く必要があります。

このメソッドは、 **Recordset** オブジェクトを **QueryDef** から作成し、その **Recordset** を関数に渡し、その関数でレコードセットを変更するクエリなどを表す SQL を再作成する必要がある場合に便利です。

## <a name="example"></a>例

次の例では、 **CopyQueryDef** メソッドを使用して既存の **Recordset** から **QueryDef** のコピーを作成し、SQL プロパティに句を追加することによってそのコピーを変更します。持続的な **QueryDef** の作成時には、SQL プロパティにスペース、セミコロン、またはラインフィードを追加できますが、SQL ステートメントに新しい句を追加するには、これらの余分な文字を削除する必要があります。

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```     

<br/>

次の例では、CopyQueryNew() の使用例を示します。

```vb
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset2 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

