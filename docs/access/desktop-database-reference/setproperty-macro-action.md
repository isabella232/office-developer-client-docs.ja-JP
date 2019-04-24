---
title: SetProperty マクロ アクション
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c5972ad630efe3afe27565924c7c6a8a2230a9f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314575"
---
# <a name="setproperty-macro-action"></a><span data-ttu-id="cfd77-102">SetProperty マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="cfd77-102">SetProperty macro action</span></span>

<span data-ttu-id="cfd77-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfd77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfd77-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span><span class="sxs-lookup"><span data-stu-id="cfd77-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span></span>

## <a name="setting"></a><span data-ttu-id="cfd77-105">Setting</span><span class="sxs-lookup"><span data-stu-id="cfd77-105">Setting</span></span>

<span data-ttu-id="cfd77-106">"SetProperty/プロパティの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cfd77-106">The **SetProperty** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfd77-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="cfd77-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cfd77-108">説明</span><span class="sxs-lookup"><span data-stu-id="cfd77-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfd77-109">コントロール名</span><span class="sxs-lookup"><span data-stu-id="cfd77-109">Control Name</span></span></p></td>
<td><p><span data-ttu-id="cfd77-110">プロパティ値を設定する対象のフィールドまたはコントロールの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="cfd77-110">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="cfd77-111">完全な構文ではなく、コントロール名のみを指定してください。</span><span class="sxs-lookup"><span data-stu-id="cfd77-111">Use only the control name, not the full syntax.</span></span> <span data-ttu-id="cfd77-112">カレント フォームまたはカレント レポートのプロパティを設定する場合は、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="cfd77-112">Leave this argument blank to set the property for the current form or report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfd77-113">プロパティ</span><span class="sxs-lookup"><span data-stu-id="cfd77-113">Property</span></span></p></td>
<td><p><span data-ttu-id="cfd77-p102">設定するプロパティを選択します。このアクションを使用して設定できるプロパティの一覧については、この記事の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfd77-p102">Select the property that you want to set. See the <strong>Remarks</strong> section in this article for a list of the properties that can be set by using this action.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfd77-116">値</span><span class="sxs-lookup"><span data-stu-id="cfd77-116">Value</span></span></p></td>
<td><p><span data-ttu-id="cfd77-p103">プロパティに対して設定する値を入力します。値が [はい] または [いいえ] のどちらかになるプロパティでは、[はい] の場合は「-1」、[いいえ] の場合は「0」を入力します。</span><span class="sxs-lookup"><span data-stu-id="cfd77-p103">Type the value that the property is to be set to. For properties whose values are either Yes or No, use <strong>-1</strong> for Yes and <strong>0</strong> for No.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cfd77-119">注釈</span><span class="sxs-lookup"><span data-stu-id="cfd77-119">Remarks</span></span>

- <span data-ttu-id="cfd77-120">"SetProperty/プロパティの設定" アクションを使用すると、コントロールの "Enabled/使用可能"、"Visible/可視"、"Locked/ロック"、"Left/左"、"Top/上"、"Width/幅"、"Height/高さ"、"Fore Color/前景色"、"Back Color/背景色"、または "Caption/標題" の各プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cfd77-120">You can use the **SetProperty** action to set the following properties of a control: **Enabled**, **Visible**, **Locked**, **Left**, **Top**, **Width**, **Height**, **Fore Color**, **Back Color**, or **Caption**.</span></span>

- <span data-ttu-id="cfd77-121">" ***value/値***" 引数に無効な値を入力すると、エラーは発生しませんが、引数がどのように解釈されるかに応じて、プロパティは別の値に変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cfd77-121">If you enter an invalid value for the ***Value*** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span>

- <span data-ttu-id="cfd77-p104">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property. If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it. If the form or report is already open, you can use the **SelectObject** action to select it. You can then use the **SetProperty** action to set the property. Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span><span class="sxs-lookup"><span data-stu-id="cfd77-p104">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property. If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it. If the form or report is already open, you can use the **SelectObject** action to select it. You can then use the **SetProperty** action to set the property. Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span></span>

- <span data-ttu-id="cfd77-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="cfd77-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="cfd77-128">例</span><span class="sxs-lookup"><span data-stu-id="cfd77-128">Example</span></span>

<span data-ttu-id="cfd77-129">次の例は、"SetProperty/プロパティの設定" アクションを使用して、 **MyTextBox**テキストボックスの表示/非表示を切り替える方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cfd77-129">The following example shows how to use the SetProperty action to toggle the visibility of the **MyTextBox** text box.</span></span>

<span data-ttu-id="cfd77-130">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="cfd77-130">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
