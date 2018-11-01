---
title: OnError マクロ アクション
TOCTitle: OnError Macro Action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e755683b4c040b37f0da12f7e67e8c400e62edb4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882141"
---
# <a name="onerror-macro-action"></a><span data-ttu-id="26f4d-102">OnError マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="26f4d-102">OnError Macro Action</span></span>

<span data-ttu-id="26f4d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="26f4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26f4d-104">**OnError** アクションを使用すると、マクロでエラーが発生したときに行われる処理を指定できます。</span><span class="sxs-lookup"><span data-stu-id="26f4d-104">You can use the **OnError** action to specify what should happen when an error occurs in a macro.</span></span>

## <a name="setting"></a><span data-ttu-id="26f4d-105">設定</span><span class="sxs-lookup"><span data-stu-id="26f4d-105">Setting</span></span>

<span data-ttu-id="26f4d-106">**OnError** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="26f4d-106">The **OnError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26f4d-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="26f4d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="26f4d-108">説明</span><span class="sxs-lookup"><span data-stu-id="26f4d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26f4d-109">Go to/移動先</span><span class="sxs-lookup"><span data-stu-id="26f4d-109">Go to</span></span></p></td>
<td><p><span data-ttu-id="26f4d-p101">エラーが発生した場合の一般的な動作を指定します。ドロップダウン ボックスの矢印をクリックし、次の設定値のいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="26f4d-p101">Specify the general behavior that should occur when an error is encountered. Click the drop-down arrow and then click one of the following settings:</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26f4d-112">設定</span><span class="sxs-lookup"><span data-stu-id="26f4d-112">Setting</span></span></p></th>
<th><p><span data-ttu-id="26f4d-113">説明</span><span class="sxs-lookup"><span data-stu-id="26f4d-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26f4d-114"><strong>Next/次のレコード</strong></span><span class="sxs-lookup"><span data-stu-id="26f4d-114"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="26f4d-p102">Microsoft Office Access 2007 では、エラーの詳細が <strong>MacroError</strong> オブジェクトに記録されますが、マクロの実行は停止されません。マクロは次のアクションを続行します。  </span><span class="sxs-lookup"><span data-stu-id="26f4d-p102">Microsoft Office Access 2007 records the details of the error in the <strong>MacroError</strong> object but does not stop the macro. The macro continues with the next action.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f4d-117"><strong>Macro Name/マクロ名</strong></span><span class="sxs-lookup"><span data-stu-id="26f4d-117"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="26f4d-118">実行中のマクロが停止され、 <strong>Macro Name/マクロ名</strong> 引数で指定されているマクロが実行されます。</span><span class="sxs-lookup"><span data-stu-id="26f4d-118">Access stops the current macro and runs the macro that is named in the <strong>Macro Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f4d-119"><strong>Fail/失敗</strong></span><span class="sxs-lookup"><span data-stu-id="26f4d-119"><strong>Fail</strong></span></span></p></td>
<td><p><span data-ttu-id="26f4d-120">実行中のマクロが停止され、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="26f4d-120">Access stops the current macro and displays an error message.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f4d-121">マクロ名</span><span class="sxs-lookup"><span data-stu-id="26f4d-121">Macro Name</span></span></p></td>
<td><p><span data-ttu-id="26f4d-122">引数に移動は、マクロ名に設定されている場合は、エラー処理に使用するマクロの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="26f4d-122">If the Go to argument is set to Macro Name, type the name of the macro to be used for error handling.</span></span> <span data-ttu-id="26f4d-123">入力した名前は、現在のマクロの [<strong>マクロ名</strong>] 列の名前と一致しなければなりません別のマクロ オブジェクトの名前を入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="26f4d-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span></span> <span data-ttu-id="26f4d-124">次の例では、 <strong>ErrorHandler</strong>マクロは、<strong>エラー時</strong>のアクションと同じマクロ オブジェクトに含まれています。</span><span class="sxs-lookup"><span data-stu-id="26f4d-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span></span> <span data-ttu-id="26f4d-125">この引数は引数に移動は、<strong>次へ</strong>] または [<strong>失敗</strong>に設定されている場合は空白のままにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26f4d-125">This argument must be left blank if the Go to argument is set to <strong>Next</strong> or <strong>Fail</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="26f4d-126">解説</span><span class="sxs-lookup"><span data-stu-id="26f4d-126">Remarks</span></span>

- <span data-ttu-id="26f4d-p104">**OnError** アクションは、通常はマクロの先頭に配置されますが、先頭以降に配置することもできます。このアクションによって設定されるルールは、アクションを実行するたびに適用されます。</span><span class="sxs-lookup"><span data-stu-id="26f4d-p104">The **OnError** action is usually placed at the beginning of a macro, but you can also place the action later in the macro. The rules established by the action will take effect whenever the action is run.</span></span>

- <span data-ttu-id="26f4d-129">ジャンプを**失敗**する引数に設定すると、アクセスはマクロで**エラー時**のアクションが存在しなかった場合と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="26f4d-129">If you set the Go to argument to **Fail**, Access behaves the same way it would if there were no **OnError** action in the macro.</span></span> <span data-ttu-id="26f4d-130">つまり、エラーが発生した場合は、マクロの実行が停止され、標準的なエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="26f4d-130">That is, if an error is encountered, Access stops the macro and displays a standard error message.</span></span> <span data-ttu-id="26f4d-131">[ **失敗** ] 設定値の主な用途は、マクロ内でそれ以前に設定したエラー処理を無効にすることです。</span><span class="sxs-lookup"><span data-stu-id="26f4d-131">The main use for the **Fail** setting is to turn off any error handling that you established earlier in a macro.</span></span>

## <a name="example"></a><span data-ttu-id="26f4d-132">例</span><span class="sxs-lookup"><span data-stu-id="26f4d-132">Example</span></span>

<span data-ttu-id="26f4d-p106">次のマクロは、" **OnError/エラー時** " アクションの使用例を示しています。この例では、エラーが発生したときに Access が " **ErrorHandler**" という名前のカスタム エラー処理マクロを実行するように、" OnError/エラー時 " アクションが指定されています。エラーが発生すると、 CatchErrors サブマクロが呼び出されます。エラー番号が 2102 の場合、特定のメッセージが表示され、マクロの実行が停止します。それ以外の場合は、エラーの内容を説明するメッセージが表示され、マクロが一時停止します。したがって、追加のトラブルシューティングを行うことができます。 ErrorHandler マクロは、 **MacroError** オブジェクトを参照するメッセージ ボックスを表示して、エラーに関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="26f4d-p106">The following macro demonstrates the use of the **OnError** action. In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs. When an error occurs, the CatchErrors submacro is called. If the error number is 2102, a specific message is displayed and macro execution is halted. Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting. The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="26f4d-139">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="26f4d-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
