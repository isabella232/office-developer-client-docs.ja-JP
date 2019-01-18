---
title: Parameter.Direction プロパティ (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3260fd3f01e8ca22d5be4f8d14f6376c31e2735a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712261"
---
# <a name="parameterdirection-property-dao"></a>Parameter.Direction プロパティ (DAO)


**適用されます**Access 2013、Office 2013。


## <a name="syntax"></a>構文

*式*です。方向

*式***パラメーター**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、 **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** クラスの定数のいずれかに設定できる長整数型 (Long) の値です。

**Direction** プロパティを使用して、パラメーターが入力パラメーター、出力パラメーター、その両方、またはプロシージャからの戻り値のいずれであるかを調べます。一部の ODBC ドライバーでは、SELECT ステートメントまたはプロシージャ コールにパラメーターの方向情報を提供しません。このような場合、方向を設定してからクエリを実行する必要があります。

たとえば、次の手順がという名前のストアド プロシージャから値を返します"取得\_従業員」。

{? get の呼び出しを =\_の従業員。

この呼び出しにより、1 つのパラメーター、つまり戻り値が作成されます。このパラメーターの方向を **dbParamOutput** または **dbParamReturnValue** に設定してから、 **[QueryDef](querydef-object-dao.md)** を実行する必要があります。

**dbParamInput** を除くすべてのパラメーターの方向を設定してから、パラメーターの値にアクセスまたは設定し、 **QueryDef** を実行する必要があります。

戻り値には **dbParamReturnValue** を使用する必要がありますが、そのオプションがドライバーまたはサーバーでサポートされていない場合は、代わりに **dbParamOutput** を使用できます。

Microsoft SQL Server ドライバーでは、すべてのプロシージャ パラメーターの **Direction** プロパティが自動的に設定されます。ODBC ドライバーの一部は、クエリ パラメーターの方向を判断できません。このような場合は、方向を設定してからクエリを実行する必要があります。

## <a name="example"></a>例

次の使用例は、 **Direction** プロパティを使用して、ODBC データ ソースへのクエリのパラメーターを設定します。

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

