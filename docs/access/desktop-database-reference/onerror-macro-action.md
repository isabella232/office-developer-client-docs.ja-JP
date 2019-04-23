---
title: OnError マクロ アクション
TOCTitle: OnError macro action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2288d64241f3289505a8b0fafb98062830b0e97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288456"
---
# <a name="onerror-macro-action"></a><span data-ttu-id="1765d-102">OnError マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="1765d-102">OnError macro action</span></span>

<span data-ttu-id="1765d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1765d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1765d-104">**OnError** アクションを使用すると、マクロでエラーが発生したときに行われる処理を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1765d-104">You can use the **OnError** action to specify what should happen when an error occurs in a macro.</span></span>

## <a name="setting"></a><span data-ttu-id="1765d-105">Setting</span><span class="sxs-lookup"><span data-stu-id="1765d-105">Setting</span></span>

<span data-ttu-id="1765d-106">**OnError** アクションの引数は次のとおりです。
</span><span class="sxs-lookup"><span data-stu-id="1765d-106">The **OnError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1765d-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="1765d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1765d-108">説明</span><span class="sxs-lookup"><span data-stu-id="1765d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1765d-109">Go to </span><span class="sxs-lookup"><span data-stu-id="1765d-109">Go to</span></span></p></td>
<td><p><span data-ttu-id="1765d-p101">エラーが発生した場合の一般的な動作を指定します。ドロップダウン ボックスの矢印をクリックし、次の設定値のいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1765d-p101">Specify the general behavior that should occur when an error is encountered. Click the drop-down arrow and then click one of the following settings:</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1765d-112">設定</span><span class="sxs-lookup"><span data-stu-id="1765d-112">Setting</span></span></p></th>
<th><p><span data-ttu-id="1765d-113">説明</span><span class="sxs-lookup"><span data-stu-id="1765d-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1765d-114"><strong>Next/次のレコード</strong></span><span class="sxs-lookup"><span data-stu-id="1765d-114"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="1765d-p102">Microsoft Office Access 2007 では、エラーの詳細が <strong>MacroError</strong> オブジェクトに記録されますが、マクロの実行は停止されません。マクロは次のアクションを続行します。  </span><span class="sxs-lookup"><span data-stu-id="1765d-p102">Microsoft Office Access 2007 records the details of the error in the <strong>MacroError</strong> object but does not stop the macro. The macro continues with the next action.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1765d-117"><strong>Macro Name/マクロ名</strong></span><span class="sxs-lookup"><span data-stu-id="1765d-117"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1765d-118">実行中のマクロが停止され、 <strong>Macro Name/マクロ名</strong> 引数で指定されているマクロが実行されます。</span><span class="sxs-lookup"><span data-stu-id="1765d-118">Access stops the current macro and runs the macro that is named in the <strong>Macro Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1765d-119"><strong>Fail/失敗</strong></span><span class="sxs-lookup"><span data-stu-id="1765d-119"><strong>Fail</strong></span></span></p></td>
<td><p><span data-ttu-id="1765d-120">実行中のマクロが停止され、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1765d-120">Access stops the current macro and displays an error message.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1765d-121">マクロ名</span><span class="sxs-lookup"><span data-stu-id="1765d-121">Macro Name</span></span></p></td>
<td><p><span data-ttu-id="1765d-122">引数 Go が [マクロ名] に設定されている場合は、エラー処理に使用するマクロの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1765d-122">If the Go to argument is set to Macro Name, type the name of the macro to be used for error handling.</span></span> <span data-ttu-id="1765d-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span><span class="sxs-lookup"><span data-stu-id="1765d-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span></span> <span data-ttu-id="1765d-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span><span class="sxs-lookup"><span data-stu-id="1765d-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span></span> <span data-ttu-id="1765d-125">Go to 引数を [<strong>次へ</strong>] または [<strong>失敗</strong>] に設定した場合、この引数は空白にしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="1765d-125">This argument must be left blank if the Go to argument is set to <strong>Next</strong> or <strong>Fail</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1765d-126">注釈</span><span class="sxs-lookup"><span data-stu-id="1765d-126">Remarks</span></span>

- <span data-ttu-id="1765d-p104">**OnError** アクションは、通常はマクロの先頭に配置されますが、先頭以降に配置することもできます。このアクションによって設定されるルールは、アクションを実行するたびに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1765d-p104">The **OnError** action is usually placed at the beginning of a macro, but you can also place the action later in the macro. The rules established by the action will take effect whenever the action is run.</span></span>

- <span data-ttu-id="1765d-129">引数 Go to 引数を**Fail**に設定すると、マクロに " **OnError/エラー**時" アクションがない場合と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="1765d-129">If you set the Go to argument to **Fail**, Access behaves the same way it would if there were no **OnError** action in the macro.</span></span> <span data-ttu-id="1765d-130">つまり、エラーが発生した場合は、マクロの実行が停止され、標準的なエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1765d-130">That is, if an error is encountered, Access stops the macro and displays a standard error message.</span></span> <span data-ttu-id="1765d-131">[ **失敗** ] 設定値の主な用途は、マクロ内でそれ以前に設定したエラー処理を無効にすることです。</span><span class="sxs-lookup"><span data-stu-id="1765d-131">The main use for the **Fail** setting is to turn off any error handling that you established earlier in a macro.</span></span>

## <a name="example"></a><span data-ttu-id="1765d-132">例</span><span class="sxs-lookup"><span data-stu-id="1765d-132">Example</span></span>

<span data-ttu-id="1765d-133">次のマクロは、"OnError/**エラー**時" アクションの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1765d-133">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="1765d-134">この例では、" **OnError** /エラー時" アクションは、エラーが発生したときに ErrorHandler という名前のカスタムエラー処理マクロを実行するように指定します。</span><span class="sxs-lookup"><span data-stu-id="1765d-134">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="1765d-135">エラーが発生すると、CatchErrors submacro が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1765d-135">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="1765d-136">エラー番号が2102の場合は、特定のメッセージが表示され、マクロの実行が停止します。</span><span class="sxs-lookup"><span data-stu-id="1765d-136">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="1765d-137">それ以外の場合は、エラーを説明するメッセージが表示され、マクロが一時停止して、追加のトラブルシューティングを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1765d-137">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="1765d-138">ErrorHandler マクロは、 **MacroError**オブジェクトを参照するメッセージボックスを表示して、エラーに関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="1765d-138">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="1765d-139">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="1765d-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
