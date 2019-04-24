---
title: Field2 プロパティ (DAO)
TOCTitle: IsComplex Property
ms:assetid: ffc90e6e-e3ee-4f9b-ca6b-615199300d45
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837318(v=office.15)
ms:contentKeyID: 48548970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d24229a0fc3122cc8a9fb20b041fc9fadc5ccb0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292784"
---
# <a name="field2iscomplex-property-dao"></a><span data-ttu-id="0ad2b-102">Field2 プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="0ad2b-102">Field2.IsComplex property (DAO)</span></span>

<span data-ttu-id="0ad2b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ad2b-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="0ad2b-104">指定されたフィールドが複数値データ型かどうかを示すブール型 ( **Boolean**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="0ad2b-104">Returns **Boolean** that indicates whether the specified field is a multi-valued data type.</span></span> <span data-ttu-id="0ad2b-105">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="0ad2b-105">Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="0ad2b-106">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="0ad2b-106">Version information</span></span>

<span data-ttu-id="0ad2b-107">追加されたバージョン: Access 2007</span><span class="sxs-lookup"><span data-stu-id="0ad2b-107">Version added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad2b-108">構文</span><span class="sxs-lookup"><span data-stu-id="0ad2b-108">Syntax</span></span>

<span data-ttu-id="0ad2b-109">*式*。IsComplex</span><span class="sxs-lookup"><span data-stu-id="0ad2b-109">*expression* .IsComplex</span></span>

<span data-ttu-id="0ad2b-110">\*式\***Field2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0ad2b-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="example"></a><span data-ttu-id="0ad2b-111">例</span><span class="sxs-lookup"><span data-stu-id="0ad2b-111">Example</span></span>

<span data-ttu-id="0ad2b-112">次の例は、複数値フィールドが含まれる Recordset 内を移動する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0ad2b-112">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="0ad2b-113">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="0ad2b-113">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub PrintStudentsAndClasses()
        Dim dbs As DAO.Database
        Dim rsStudents As DAO.Recordset2  'Recordset for students
        Dim rsClasses As DAO.Recordset2  'Recordset for classes
        Dim fld As DAO.Field2
    
        'open the database
        Set dbs = CurrentDb()
    
        'get the table of students
        Set rsStudents = dbs.OpenRecordset("tblStudents")
    
        'loop through the students
        Do While Not rsStudents.EOF
            
            'get the classes field
            Set fld = rsStudents("Classes")
    
            'get the classes Recordset
            'make sure the field is a multi-valued field before
            'getting a Recordset object
            If fld.IsComplex Then
                Set rsClasses = fld.Value
            End If
    
            'access all records in the Recordset
            If Not (rsClasses.BOF And rsClasses.EOF) Then
                rsClasses.MoveLast
                rsClasses.MoveFirst
            End If
    
            'print the student and number of classes
            Debug.Print rsStudents("FirstName") & " " & rsStudents("LastName"), _
                "Number of classes: " & rsClasses.RecordCount
    
            'print the classes for this student
            Do While Not rsClasses.EOF
                Debug.Print , rsClasses("Value")
                rsClasses.MoveNext
            Loop
    
            'close the Classes Recordset
            rsClasses.Close
    
            'get the next student
            rsStudents.MoveNext
    
        Loop
        
        'cleanup
        rsStudents.Close
    
        Set fld = Nothing
        Set rsStudents = Nothing
        Set dbs = Nothing
    
    End Sub
```
