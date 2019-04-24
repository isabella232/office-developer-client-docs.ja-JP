---
title: Error. Number プロパティ (DAO)
TOCTitle: Number Property
ms:assetid: 2fb94dca-f990-04f8-bbd2-9919d28de75a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192259(v=office.15)
ms:contentKeyID: 48544013
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053363
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 257c403951eff5bbb2f37de8b38a1c63a3445285
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293498"
---
# <a name="errornumber-property-dao"></a><span data-ttu-id="4ffb7-102">Error. Number プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="4ffb7-102">Error.Number property (DAO)</span></span>


<span data-ttu-id="4ffb7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ffb7-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="4ffb7-104">エラーを示す数値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4ffb7-104">Returns a numeric value specifying an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ffb7-105">構文</span><span class="sxs-lookup"><span data-stu-id="4ffb7-105">Syntax</span></span>

<span data-ttu-id="4ffb7-106">*式*。件数</span><span class="sxs-lookup"><span data-stu-id="4ffb7-106">*expression* .Number</span></span>

<span data-ttu-id="4ffb7-107">*式*: **Error** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="4ffb7-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ffb7-108">解説</span><span class="sxs-lookup"><span data-stu-id="4ffb7-108">Remarks</span></span>

<span data-ttu-id="4ffb7-p101">**Number** プロパティを使用して、発生したエラーを特定します。このプロパティの値は、エラーの状態を表す一意のトラップ番号に対応しています。</span><span class="sxs-lookup"><span data-stu-id="4ffb7-p101">Use the **Number** property to determine the error that occurred. The value of the property corresponds to a unique trap number that corresponds to an error condition.</span></span>

## <a name="example"></a><span data-ttu-id="4ffb7-111">例</span><span class="sxs-lookup"><span data-stu-id="4ffb7-111">Example</span></span>

<span data-ttu-id="4ffb7-112">次の使用例は、エラーを強制的に発生させ、トラップし、生成された **Error** オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="4ffb7-112">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

