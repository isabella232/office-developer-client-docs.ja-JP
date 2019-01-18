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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703218"
---
# <a name="setproperty-macro-action"></a><span data-ttu-id="70b9b-102">SetProperty マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="70b9b-102">SetProperty macro action</span></span>

<span data-ttu-id="70b9b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="70b9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70b9b-104">**SetProperty**アクションを使用すると、フォームまたはレポート上のコントロールのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="70b9b-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span></span>

## <a name="setting"></a><span data-ttu-id="70b9b-105">設定値</span><span class="sxs-lookup"><span data-stu-id="70b9b-105">Setting</span></span>

<span data-ttu-id="70b9b-106">**SetProperty**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="70b9b-106">The **SetProperty** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70b9b-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="70b9b-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="70b9b-108">説明</span><span class="sxs-lookup"><span data-stu-id="70b9b-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70b9b-109">コントロール名</span><span class="sxs-lookup"><span data-stu-id="70b9b-109">Control Name</span></span></p></td>
<td><p><span data-ttu-id="70b9b-110">フィールドまたはプロパティの値を設定するコントロールの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="70b9b-110">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="70b9b-111">コントロール名だけをしない完全な構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="70b9b-111">Use only the control name, not the full syntax.</span></span> <span data-ttu-id="70b9b-112">カレント フォームまたはカレント レポートのプロパティを設定する場合は、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="70b9b-112">Leave this argument blank to set the property for the current form or report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b9b-113">プロパティ</span><span class="sxs-lookup"><span data-stu-id="70b9b-113">Property</span></span></p></td>
<td><p><span data-ttu-id="70b9b-114">設定するプロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="70b9b-114">Select the property that you want to set.</span></span> <span data-ttu-id="70b9b-115">このアクションを使用して設定できるプロパティの一覧については、この資料の<strong>「解説」</strong>セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="70b9b-115">See the <strong>Remarks</strong> section in this article for a list of the properties that can be set by using this action.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b9b-116">値</span><span class="sxs-lookup"><span data-stu-id="70b9b-116">Value</span></span></p></td>
<td><p><span data-ttu-id="70b9b-117">プロパティを設定する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70b9b-117">Type the value that the property is to be set to.</span></span> <span data-ttu-id="70b9b-118">プロパティの値を持つか、[はい] またはいいえ、 <strong>-1</strong>を使用して、[はい] を [いいえ] は<strong>0</strong></span><span class="sxs-lookup"><span data-stu-id="70b9b-118">For properties whose values are either Yes or No, use <strong>-1</strong> for Yes and <strong>0</strong> for No.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="70b9b-119">解説</span><span class="sxs-lookup"><span data-stu-id="70b9b-119">Remarks</span></span>

- <span data-ttu-id="70b9b-120">**SetProperty**操作を使用するには、コントロールの次のプロパティを設定するのには:**有効になっている**、**表示**、**ロックされている**、**左**、**上**、**幅**、**高さ\*\*\*\*前景の色**、**背景色**、または**キャプション**です。</span><span class="sxs-lookup"><span data-stu-id="70b9b-120">You can use the **SetProperty** action to set the following properties of a control: **Enabled**, **Visible**, **Locked**, **Left**, **Top**, **Width**, **Height**, **Fore Color**, **Back Color**, or **Caption**.</span></span>

- <span data-ttu-id="70b9b-121">引数の***値***に無効な値を入力すると、エラーは発生しませんが、アクセスは、引数を解釈する方法によって、別の値にプロパティを変更する場合があります。</span><span class="sxs-lookup"><span data-stu-id="70b9b-121">If you enter an invalid value for the ***Value*** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span>

- <span data-ttu-id="70b9b-122">フォームまたはレポートのプロパティを設定する対象のコントロールを含むを選択するアクションを実行した後にする場合にのみ、独立マクロ**SetProperty**操作を使用できます。</span><span class="sxs-lookup"><span data-stu-id="70b9b-122">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property.</span></span> <span data-ttu-id="70b9b-123">フォームまたはレポートが開いていない場合は、] を選択して、 **OpenForm**または**OpenReport**アクションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="70b9b-123">If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it.</span></span> <span data-ttu-id="70b9b-124">フォームまたはレポートが既に開いている場合をオンに**します**を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="70b9b-124">If the form or report is already open, you can use the **SelectObject** action to select it.</span></span> <span data-ttu-id="70b9b-125">プロパティを設定するのには、 **SetProperty**操作を使用できます。</span><span class="sxs-lookup"><span data-stu-id="70b9b-125">You can then use the **SetProperty** action to set the property.</span></span> <span data-ttu-id="70b9b-126">オブジェクトを選択することは、プロパティを設定する対象のコントロールと同じフォームまたはレポート上のコントロールに埋め込まれているマクロで**SetProperty**操作を使用する場合に必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="70b9b-126">Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span></span>

- <span data-ttu-id="70b9b-127">VBA モジュールでは、 **SetProperty**アクションを実行するには、 **DoCmd**オブジェクトの**SetProperty**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="70b9b-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="70b9b-128">使用例</span><span class="sxs-lookup"><span data-stu-id="70b9b-128">Example</span></span>

<span data-ttu-id="70b9b-129">**MyTextBox** ] テキスト ボックスの表示/非表示を切り替えるには、SetProperty 操作を使用する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="70b9b-129">The following example shows how to use the SetProperty action to toggle the visibility of the **MyTextBox** text box.</span></span>

<span data-ttu-id="70b9b-130">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="70b9b-130">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
