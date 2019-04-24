---
title: 'エラー: Description プロパティ (DAO)'
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1d7e949771e764c22e93ef56059930ccf39584ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293505"
---
# <a name="errordescription-property-dao"></a><span data-ttu-id="142e4-102">エラー: Description プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="142e4-102">Error.Description property (DAO)</span></span>


<span data-ttu-id="142e4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="142e4-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="142e4-104">エラーについて説明する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="142e4-104">Returns a descriptive string associated with an error.</span></span> <span data-ttu-id="142e4-105">これは、 **Error** オブジェクトの既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="142e4-105">This is the default property for the **Error** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="142e4-106">構文</span><span class="sxs-lookup"><span data-stu-id="142e4-106">Syntax</span></span>

<span data-ttu-id="142e4-107">*式*。Description</span><span class="sxs-lookup"><span data-stu-id="142e4-107">*expression* .Description</span></span>

<span data-ttu-id="142e4-108">*式*: **Error** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="142e4-108">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="142e4-109">解説</span><span class="sxs-lookup"><span data-stu-id="142e4-109">Remarks</span></span>

<span data-ttu-id="142e4-p102">**Description** プロパティは、エラーの簡単な説明で構成されます。プログラムで対処できないエラー、または処理することが望ましくないエラーについては、このプロパティを使用してユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="142e4-p102">The **Description** property comprises a short description of the error. Use this property to alert the user about an error that you cannot or do not want to handle.</span></span>

## <a name="example"></a><span data-ttu-id="142e4-112">例</span><span class="sxs-lookup"><span data-stu-id="142e4-112">Example</span></span>

<span data-ttu-id="142e4-113">次の使用例は、エラーを強制的に発生させ、トラップし、生成された Error オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="142e4-113">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting Error object.</span></span>

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

