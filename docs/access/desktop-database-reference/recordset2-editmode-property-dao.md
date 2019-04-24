---
title: Recordset2 プロパティ (DAO)
TOCTitle: EditMode Property
ms:assetid: fd61ea2b-e7d7-195f-4114-87e54eba2451
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837240(v=office.15)
ms:contentKeyID: 48548914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053080
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d4043a442bec8c5ce421d85de6256eb9c5cb353f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307351"
---
# <a name="recordset2editmode-property-dao"></a><span data-ttu-id="7aebc-102">Recordset2 プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="7aebc-102">Recordset2.EditMode property (DAO)</span></span>


<span data-ttu-id="7aebc-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7aebc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7aebc-104">カレント レコードの編集状態を示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="7aebc-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aebc-105">構文</span><span class="sxs-lookup"><span data-stu-id="7aebc-105">Syntax</span></span>

<span data-ttu-id="7aebc-106">*式*。EditMode</span><span class="sxs-lookup"><span data-stu-id="7aebc-106">*expression* .EditMode</span></span>

<span data-ttu-id="7aebc-107">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="7aebc-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aebc-108">注釈</span><span class="sxs-lookup"><span data-stu-id="7aebc-108">Remarks</span></span>

<span data-ttu-id="7aebc-p101">戻り値は、編集状態を示す長整数型 ( **Long**) の値です。使用できる値は、 **[EditModeEnum](editmodeenum-enumeration-dao.md)** クラスの定数のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="7aebc-p101">The return value is a **Long** that indicates the state of editing. The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="7aebc-p102">**EditMode** プロパティは、検証中のエラーなどによって、編集プロセスが中断した場合に便利です。 **EditMode** プロパティの値を使用して、 **[Update](recordset2-update-method-dao.md)** メソッドと **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** メソッドのいずれを使用する必要があるかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="7aebc-p102">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation. You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset2-update-method-dao.md)** or **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="7aebc-113">**[LockEdits](recordset2-lockedits-property-dao.md)** プロパティの設定値が **True** で、 **EditMode** プロパティの設定値が **dbEditInProgress** であるかどうかを確認して、現在のページがロックされているかどうかを判断することもできます。</span><span class="sxs-lookup"><span data-stu-id="7aebc-113">You can also check to see if the **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="7aebc-114">例</span><span class="sxs-lookup"><span data-stu-id="7aebc-114">Example</span></span>

<span data-ttu-id="7aebc-p103">次の使用例は、さまざまな条件下での **EditMode** プロパティの値を示します。このプロシージャを実行するには、EditModeOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="7aebc-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span></span>

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Show the EditMode property under different editing 
     ' states. 
     With rstEmployees 
     EditModeOutput "Before any Edit or AddNew:", .EditMode 
     .Edit 
     EditModeOutput "After Edit:", .EditMode 
     .Update 
     EditModeOutput "After Update:", .EditMode 
     .AddNew 
     EditModeOutput "After AddNew:", .EditMode 
     .CancelUpdate 
     EditModeOutput "After CancelUpdate:", .EditMode 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function EditModeOutput(strTemp As String, _ 
     intEditMode As Integer) 
     
     ' Print report based on the value of the EditMode 
     ' property. 
     Debug.Print strTemp 
     Debug.Print " EditMode = "; 
     
     Select Case intEditMode 
     Case dbEditNone 
     Debug.Print "dbEditNone" 
     Case dbEditInProgress 
     Debug.Print "dbEditInProgress" 
     Case dbEditAdd 
     Debug.Print "dbEditAdd" 
     End Select 
     
    End Function
```
