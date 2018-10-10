---
title: Error.Source プロパティ (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b9aafe1b16b3d989a81ff21f97bd4b6d10f79de3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478475"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="1f091-102">Error.Source プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="1f091-102">Error.Source Property (DAO)</span></span>


<span data-ttu-id="1f091-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f091-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="1f091-104">エラーの発生源のオブジェクト名またはアプリケーション名を取得します。</span><span class="sxs-lookup"><span data-stu-id="1f091-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f091-105">構文</span><span class="sxs-lookup"><span data-stu-id="1f091-105">Syntax</span></span>

<span data-ttu-id="1f091-106">*式*です。ソース</span><span class="sxs-lookup"><span data-stu-id="1f091-106">*expression* .Source</span></span>

<span data-ttu-id="1f091-107">\*式\***エラー**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="1f091-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f091-108">注釈</span><span class="sxs-lookup"><span data-stu-id="1f091-108">Remarks</span></span>

<span data-ttu-id="1f091-p101">**Source** プロパティの値は、通常、オブジェクトのクラス名またはプログラム識別子になります。 **Source** プロパティを使用すると、別のアプリケーションのオブジェクトで発生したエラーをコードで処理できない場合、ユーザーにその情報を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="1f091-p101">The **Source** property value is usually the object's class name or programmatic ID. Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="1f091-111">などの Microsoft Excel にアクセスする場合は、「0 除算」エラーが生成されます、Microsoft Excel は、Microsoft Excel のコードにエラーが**Error.Number**を設定し、始めますに**Source**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1f091-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="1f091-112">エラーが Microsoft Office Excel によって呼び出された別のオブジェクトで発生した場合は、Microsoft Office Excel がそのエラーを解釈し、 **Error.Number** を Microsoft Office Excel コードに設定することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1f091-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="1f091-113">ただし、他の **Error** オブジェクトのプロパティ ( **Source** プロパティを含む) は、エラーの発生源となったオブジェクトが設定した値を保持します。</span><span class="sxs-lookup"><span data-stu-id="1f091-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="1f091-114">**Source** プロパティは、常にエラーの発生源となったオブジェクトの名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="1f091-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="1f091-p103">すべてのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。エラー処理ルーチンが失敗した場合、 **[Error](error-object-dao.md)** オブジェクトの情報を使用してユーザーにエラーに関する説明を提供でき、 **Source** プロパティや他の **Error** プロパティを使用すると、ユーザーにエラーの発生源となったオブジェクトの情報、エラーの説明などを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="1f091-p103">Based on all of the error documentation, you can write code that will handle the error appropriately. If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1f091-p104">他のオブジェクトへのアクセス時に発生したエラーを処理する場合、<STRONG>On Error GoTo</STRONG> より <STRONG>On Error Resume Next</STRONG> ステートメントの使用をお勧めします。オブジェクトとの各相互作用の後に <STRONG>Error</STRONG> オブジェクトのプロパティを確認すると、エラーの発生時にコードがアクセスしていたオブジェクトを明確にすることができます。このため、<STRONG>Error.Number</STRONG> にエラー コードを配置したオブジェクトや、エラーの発生源となったオブジェクト (<STRONG>Error.Source</STRONG>) を確認できます。</span><span class="sxs-lookup"><span data-stu-id="1f091-p104">The <STRONG>On Error Resume Next</STRONG> construct may be preferable to <STRONG>On Error GoTo</STRONG> when dealing with errors generated during access to other objects. Checking the <STRONG>Error</STRONG> object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred. Thus, you can be sure which object placed the error code in <STRONG>Error.Number</STRONG>, as well as which object originally generated the error (<STRONG>Error.Source</STRONG>).</span></span></P>



## <a name="example"></a><span data-ttu-id="1f091-120">例</span><span class="sxs-lookup"><span data-stu-id="1f091-120">Example</span></span>

<span data-ttu-id="1f091-121">この例では、エラーを発生させてトラップし、 **Error** オブジェクトの **Description**、 **Number**、 **Source**、 **HelpContext**、および **HelpFile** の各プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="1f091-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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