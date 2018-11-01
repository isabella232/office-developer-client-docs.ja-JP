---
title: Submacro マクロ ステートメント
TOCTitle: Submacro Macro Statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de0d7066927e3a3cf034197c15f4330302801c0a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885928"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="daf03-102">Submacro マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="daf03-102">Submacro Macro Statement</span></span>

<span data-ttu-id="daf03-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="daf03-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="daf03-104">**サブマクロ**ステートメントは、マクロ デザイナー ウィンドウで、別のマクロを定義します。</span><span class="sxs-lookup"><span data-stu-id="daf03-104">The **Submacro** statement defines a seperate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="daf03-105">設定</span><span class="sxs-lookup"><span data-stu-id="daf03-105">Setting</span></span>

<span data-ttu-id="daf03-106">**サブマクロ**のアクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="daf03-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="daf03-107">引数</span><span class="sxs-lookup"><span data-stu-id="daf03-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="daf03-108">必須</span><span class="sxs-lookup"><span data-stu-id="daf03-108">Required</span></span></p></th>
<th><p><span data-ttu-id="daf03-109">説明</span><span class="sxs-lookup"><span data-stu-id="daf03-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf03-110">名前</span><span class="sxs-lookup"><span data-stu-id="daf03-110">Name</span></span></p></td>
<td><p><span data-ttu-id="daf03-111">はい</span><span class="sxs-lookup"><span data-stu-id="daf03-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="daf03-112">マクロの名前として表示する文字列。</span><span class="sxs-lookup"><span data-stu-id="daf03-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="daf03-113">例</span><span class="sxs-lookup"><span data-stu-id="daf03-113">Example</span></span>

<span data-ttu-id="daf03-p101">次のマクロは、" **OnError/エラー時** " アクションの使用例を示しています。この例では、エラーが発生したときに Access が " **ErrorHandler**" という名前のカスタム エラー処理マクロを実行するように、" OnError/エラー時 " アクションが指定されています。エラーが発生すると、 CatchErrors サブマクロが呼び出されます。エラー番号が 2102 の場合、特定のメッセージが表示され、マクロの実行が停止します。それ以外の場合は、エラーの内容を説明するメッセージが表示され、マクロが一時停止します。したがって、追加のトラブルシューティングを行うことができます。 ErrorHandler マクロは、 **MacroError** オブジェクトを参照するメッセージ ボックスを表示して、エラーに関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="daf03-p101">The following macro demonstrates the use of the **OnError** action. In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs. When an error occurs, the CatchErrors submacro is called. If the error number is 2102, a specific message is displayed and macro execution is halted. Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting. The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="daf03-120">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="daf03-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
