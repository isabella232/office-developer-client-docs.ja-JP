---
title: StopMacro マクロ アクション
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308499"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="46788-102">StopMacro マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="46788-102">StopMacro macro action</span></span>

<span data-ttu-id="46788-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="46788-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46788-104">**StopMacro** アクションを使用して、現在実行中のマクロを中止できます。</span><span class="sxs-lookup"><span data-stu-id="46788-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="46788-105">Setting</span><span class="sxs-lookup"><span data-stu-id="46788-105">Setting</span></span>

<span data-ttu-id="46788-106">**StopMacro** アクションには引数はありません。</span><span class="sxs-lookup"><span data-stu-id="46788-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="46788-107">注釈</span><span class="sxs-lookup"><span data-stu-id="46788-107">Remarks</span></span>

<span data-ttu-id="46788-p101">通常、このアクションは、マクロを中止する必要が生じた場合に使用します。このアクションが定義されているマクロ内のアクション行に条件式を指定できます。条件式の評価が **True** (-1) の場合、Microsoft Access はマクロを中止します。</span><span class="sxs-lookup"><span data-stu-id="46788-p101">You typically use this action when a condition makes it necessary to stop the macro. You can use a conditional expression in the macro's action row that contains this action. When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="46788-p102">たとえば、カスタム ダイアログ ボックスに入力された日付の注文の合計が表示されるフォームを開くマクロを作成するとします。条件式を使用すると、ダイアログ ボックスの [ **注文日**] コントロールの日付が必ず有効になるように指定できます。有効でない場合は、" **MessageBox/メッセージボックス** " アクションによってエラー メッセージを表示し、" **StopMacro/マクロの中止** " アクションでマクロを中止することができます。</span><span class="sxs-lookup"><span data-stu-id="46788-p102">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box. You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date. If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="46788-114">マクロ内で " **Echo/エコー** " アクションや " **SetWarnings/メッセージの設定** " アクションを使用して、エコーまたはシステム メッセージの表示がオフになっている場合は、" **StopMacros/マクロの中止** " アクションを実行すると、これらの設定が自動的にオンに戻ります。</span><span class="sxs-lookup"><span data-stu-id="46788-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="46788-115">このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="46788-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="46788-116">例</span><span class="sxs-lookup"><span data-stu-id="46788-116">Example</span></span>

<span data-ttu-id="46788-117">次のマクロは、"OnError/**エラー**時" アクションの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="46788-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="46788-118">この例では、" **OnError** /エラー時" アクションは、エラーが発生したときに ErrorHandler という名前のカスタムエラー処理マクロを実行するように指定します。</span><span class="sxs-lookup"><span data-stu-id="46788-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="46788-119">エラーが発生すると、CatchErrors submacro が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46788-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="46788-120">エラー番号が2102の場合は、特定のメッセージが表示され、マクロの実行が停止します。</span><span class="sxs-lookup"><span data-stu-id="46788-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="46788-121">それ以外の場合は、エラーを説明するメッセージが表示され、マクロが一時停止して、追加のトラブルシューティングを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="46788-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="46788-122">ErrorHandler マクロは、 **MacroError**オブジェクトを参照するメッセージボックスを表示して、エラーに関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="46788-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="46788-123">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="46788-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
