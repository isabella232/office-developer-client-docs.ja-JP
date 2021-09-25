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
ms.localizationpriority: medium
ms.openlocfilehash: e8b8168383433a9b35523dd866afe98396b1e9f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606577"
---
# <a name="parameterdirection-property-dao"></a>Parameter.Direction プロパティ (DAO)


**適用先**: Access 2013、Office 2013


## <a name="syntax"></a>構文

*式* .方向

*式* Parameter オブジェクトを表 **す変数** 。

## <a name="remarks"></a>注釈

設定値または戻り値は、 **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** クラスの定数のいずれかに設定できる長整数型 (Long) の値です。

**Direction** プロパティを使用して、パラメーターが入力パラメーター、出力パラメーター、その両方、またはプロシージャからの戻り値のいずれであるかを調べます。一部の ODBC ドライバーでは、SELECT ステートメントまたはプロシージャ コールにパラメーターの方向情報を提供しません。このような場合、方向を設定してからクエリを実行する必要があります。

たとえば、次の手順では、"従業員の取得" という名前のストアド プロシージャから値を \_ 返します。

{? = 呼び出しは \_ 従業員を取得する}

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

