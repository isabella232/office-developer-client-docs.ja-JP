---
title: Submacro マクロ ステートメント
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caabfb0f4e90134c10d5ab728f19e1fd2a4437dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308471"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="7ac4f-102">Submacro マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="7ac4f-102">Submacro macro statement</span></span>

<span data-ttu-id="7ac4f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ac4f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ac4f-104">**Submacro**ステートメントは、マクロデザイナーウィンドウで別のマクロを定義します。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="7ac4f-105">Setting</span><span class="sxs-lookup"><span data-stu-id="7ac4f-105">Setting</span></span>

<span data-ttu-id="7ac4f-106">Submacro アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ac4f-107">引数</span><span class="sxs-lookup"><span data-stu-id="7ac4f-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="7ac4f-108">必須</span><span class="sxs-lookup"><span data-stu-id="7ac4f-108">Required</span></span></p></th>
<th><p><span data-ttu-id="7ac4f-109">説明</span><span class="sxs-lookup"><span data-stu-id="7ac4f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ac4f-110">名前</span><span class="sxs-lookup"><span data-stu-id="7ac4f-110">Name</span></span></p></td>
<td><p><span data-ttu-id="7ac4f-111">はい</span><span class="sxs-lookup"><span data-stu-id="7ac4f-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="7ac4f-112">マクロの名前として表示する文字列。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="7ac4f-113">例</span><span class="sxs-lookup"><span data-stu-id="7ac4f-113">Example</span></span>

<span data-ttu-id="7ac4f-114">次のマクロは、"OnError/**エラー**時" アクションの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="7ac4f-115">この例では、" **OnError** /エラー時" アクションは、エラーが発生したときに ErrorHandler という名前のカスタムエラー処理マクロを実行するように指定します。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="7ac4f-116">エラーが発生すると、CatchErrors submacro が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="7ac4f-117">エラー番号が2102の場合は、特定のメッセージが表示され、マクロの実行が停止します。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="7ac4f-118">それ以外の場合は、エラーを説明するメッセージが表示され、マクロが一時停止して、追加のトラブルシューティングを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="7ac4f-119">ErrorHandler マクロは、 **MacroError**オブジェクトを参照するメッセージボックスを表示して、エラーに関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="7ac4f-120">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="7ac4f-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
