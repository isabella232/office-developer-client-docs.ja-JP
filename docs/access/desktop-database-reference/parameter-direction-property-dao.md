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
ms.openlocfilehash: 4612b578971f59744e25c15d3762cc893f6f71ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476863"
---
# <a name="parameterdirection-property-dao"></a><span data-ttu-id="91740-102">Parameter.Direction プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="91740-102">Parameter.Direction Property (DAO)</span></span>


<span data-ttu-id="91740-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="91740-103">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="syntax"></a><span data-ttu-id="91740-104">構文</span><span class="sxs-lookup"><span data-stu-id="91740-104">Syntax</span></span>

<span data-ttu-id="91740-105">*式*です。方向</span><span class="sxs-lookup"><span data-stu-id="91740-105">*expression* .Direction</span></span>

<span data-ttu-id="91740-106">\*式\***パラメーター**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="91740-106">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91740-107">注釈</span><span class="sxs-lookup"><span data-stu-id="91740-107">Remarks</span></span>

<span data-ttu-id="91740-108">設定値または戻り値は、 **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** クラスの定数のいずれかに設定できる長整数型 (Long) の値です。</span><span class="sxs-lookup"><span data-stu-id="91740-108">The setting or return value is a Long that can be set to one of the **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="91740-p101">**Direction** プロパティを使用して、パラメーターが入力パラメーター、出力パラメーター、その両方、またはプロシージャからの戻り値のいずれであるかを調べます。一部の ODBC ドライバーでは、SELECT ステートメントまたはプロシージャ コールにパラメーターの方向情報を提供しません。このような場合、方向を設定してからクエリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91740-p101">Use the **Direction** property to determine whether the parameter is an input parameter, output parameter, both, or the return value from the procedure. Some ODBC drivers do not provide information on the direction of parameters to a SELECT statement or procedure call. In these cases, it is necessary to set the direction prior to executing the query.</span></span>

<span data-ttu-id="91740-112">たとえば、次の手順がという名前のストアド プロシージャから値を返します"取得\_従業員」。</span><span class="sxs-lookup"><span data-stu-id="91740-112">For example, the following procedure returns a value from a stored procedure named "get\_employees":</span></span>

<span data-ttu-id="91740-113">{?</span><span class="sxs-lookup"><span data-stu-id="91740-113"></span></span> <span data-ttu-id="91740-114">get の呼び出しを =\_の従業員。</span><span class="sxs-lookup"><span data-stu-id="91740-114">= call get\_employees}</span></span>

<span data-ttu-id="91740-p103">この呼び出しにより、1 つのパラメーター、つまり戻り値が作成されます。このパラメーターの方向を **dbParamOutput** または **dbParamReturnValue** に設定してから、 **[QueryDef](querydef-object-dao.md)** を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91740-p103">This call produces one parameter — the return value. You need to set the direction of this parameter to **dbParamOutput** or **dbParamReturnValue** before executing the **[QueryDef](querydef-object-dao.md)**.</span></span>

<span data-ttu-id="91740-117">**dbParamInput** を除くすべてのパラメーターの方向を設定してから、パラメーターの値にアクセスまたは設定し、 **QueryDef** を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91740-117">You need to set all parameter directions except **dbParamInput** before accessing or setting the values of the parameters and before executing the **QueryDef**.</span></span>

<span data-ttu-id="91740-118">戻り値には **dbParamReturnValue** を使用する必要がありますが、そのオプションがドライバーまたはサーバーでサポートされていない場合は、代わりに **dbParamOutput** を使用できます。</span><span class="sxs-lookup"><span data-stu-id="91740-118">You should use **dbParamReturnValue** for return values, but in cases where that option is not supported by the driver or the server, you can use **dbParamOutput** instead.</span></span>

<span data-ttu-id="91740-p104">Microsoft SQL Server ドライバーでは、すべてのプロシージャ パラメーターの **Direction** プロパティが自動的に設定されます。ODBC ドライバーの一部は、クエリ パラメーターの方向を判断できません。このような場合は、方向を設定してからクエリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91740-p104">The Microsoft SQL Server driver automatically sets the **Direction** property for all procedure parameters. Not all ODBC drivers can determine the direction of a query parameter. In these cases, it is necessary to set the direction prior to executing the query.</span></span>

## <a name="example"></a><span data-ttu-id="91740-122">例</span><span class="sxs-lookup"><span data-stu-id="91740-122">Example</span></span>

<span data-ttu-id="91740-123">次の使用例は、 **Direction** プロパティを使用して、ODBC データ ソースへのクエリのパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="91740-123">This example uses the **Direction** property to configure the parameters of a query to an ODBC data source.</span></span>

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

