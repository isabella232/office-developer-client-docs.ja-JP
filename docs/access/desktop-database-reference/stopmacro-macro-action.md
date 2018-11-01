---
title: StopMacro マクロ アクション
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3880b57e235520e3351ef16282fb8883d93b11e3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873713"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="6cef8-102">StopMacro マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="6cef8-102">StopMacro Macro Action</span></span>

<span data-ttu-id="6cef8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6cef8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6cef8-104">" **StopMacro/マクロの中止** " アクションを使用すると、現在実行中のマクロを中止できます。</span><span class="sxs-lookup"><span data-stu-id="6cef8-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="6cef8-105">設定</span><span class="sxs-lookup"><span data-stu-id="6cef8-105">Setting</span></span>

<span data-ttu-id="6cef8-106">" **StopMacro/マクロの中止** " アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="6cef8-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cef8-107">注釈</span><span class="sxs-lookup"><span data-stu-id="6cef8-107">Remarks</span></span>

<span data-ttu-id="6cef8-108">通常、このアクションは、マクロを中止する必要が生じた場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="6cef8-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="6cef8-109">このアクションが定義されているマクロ内のアクション行に条件式を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6cef8-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="6cef8-110">式は、 **True** (-1) に評価されると、Microsoft Access はマクロを停止します。</span><span class="sxs-lookup"><span data-stu-id="6cef8-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="6cef8-p102">たとえば、カスタム ダイアログ ボックスに入力された日付の注文の合計が表示されるフォームを開くマクロを作成するとします。条件式を使用すると、ダイアログ ボックスの [ **注文日**] コントロールの日付が必ず有効になるように指定できます。有効でない場合は、" **MessageBox/メッセージボックス** " アクションによってエラー メッセージを表示し、" **StopMacro/マクロの中止** " アクションでマクロを中止することができます。</span><span class="sxs-lookup"><span data-stu-id="6cef8-p102">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box. You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date. If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="6cef8-114">マクロ内で " **Echo/エコー** " アクションや " **SetWarnings/メッセージの設定** " アクションを使用して、エコーまたはシステム メッセージの表示がオフになっている場合は、" **StopMacros/マクロの中止** " アクションを実行すると、これらの設定が自動的にオンに戻ります。</span><span class="sxs-lookup"><span data-stu-id="6cef8-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="6cef8-115">このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="6cef8-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="6cef8-116">例</span><span class="sxs-lookup"><span data-stu-id="6cef8-116">Example</span></span>

<span data-ttu-id="6cef8-p103">次のマクロは、" **OnError/エラー時** " アクションの使用例を示しています。この例では、エラーが発生したときに Access が " **ErrorHandler**" という名前のカスタム エラー処理マクロを実行するように、" OnError/エラー時 " アクションが指定されています。エラーが発生すると、 CatchErrors サブマクロが呼び出されます。エラー番号が 2102 の場合、特定のメッセージが表示され、マクロの実行が停止します。それ以外の場合は、エラーの内容を説明するメッセージが表示され、マクロが一時停止します。したがって、追加のトラブルシューティングを行うことができます。 ErrorHandler マクロは、 **MacroError** オブジェクトを参照するメッセージ ボックスを表示して、エラーに関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="6cef8-p103">The following macro demonstrates the use of the **OnError** action. In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs. When an error occurs, the CatchErrors submacro is called. If the error number is 2102, a specific message is displayed and macro execution is halted. Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting. The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="6cef8-123">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="6cef8-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
