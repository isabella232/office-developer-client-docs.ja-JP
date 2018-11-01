---
title: Error.Description プロパティ (DAO)
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
ms.openlocfilehash: 2de4c87832956fb690f67f734d418a855b179d8c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870339"
---
# <a name="errordescription-property-dao"></a><span data-ttu-id="12aab-102">Error.Description プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="12aab-102">Error.Description Property (DAO)</span></span>


<span data-ttu-id="12aab-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="12aab-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="12aab-p101">エラーについて説明する文字列を取得します。これは、 **Error** オブジェクトの既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="12aab-p101">Returns a descriptive string associated with an error. This is the default property for the **Error** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="12aab-106">構文</span><span class="sxs-lookup"><span data-stu-id="12aab-106">Syntax</span></span>

<span data-ttu-id="12aab-107">*式*です。説明</span><span class="sxs-lookup"><span data-stu-id="12aab-107">*expression* .Description</span></span>

<span data-ttu-id="12aab-108">\*式\***エラー**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="12aab-108">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="12aab-109">注釈</span><span class="sxs-lookup"><span data-stu-id="12aab-109">Remarks</span></span>

<span data-ttu-id="12aab-p102">**Description** プロパティは、エラーの簡単な説明で構成されます。プログラムで対処できないエラー、または処理することが望ましくないエラーについては、このプロパティを使用してユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="12aab-p102">The **Description** property comprises a short description of the error. Use this property to alert the user about an error that you cannot or do not want to handle.</span></span>

## <a name="example"></a><span data-ttu-id="12aab-112">例</span><span class="sxs-lookup"><span data-stu-id="12aab-112">Example</span></span>

<span data-ttu-id="12aab-113">次の使用例は、エラーを強制的に発生させ、トラップし、生成された Error オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="12aab-113">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting Error object.</span></span>

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

