---
title: ClearMacroError マクロ アクション
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296375"
---
# <a name="clearmacroerror-macro-action"></a><span data-ttu-id="aebbb-102">ClearMacroError マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="aebbb-102">ClearMacroError macro action</span></span>


<span data-ttu-id="aebbb-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="aebbb-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="aebbb-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span><span class="sxs-lookup"><span data-stu-id="aebbb-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span></span>

## <a name="setting"></a><span data-ttu-id="aebbb-105">Setting</span><span class="sxs-lookup"><span data-stu-id="aebbb-105">Setting</span></span>

<span data-ttu-id="aebbb-106">"ClaerMacroError/マクロエラーのクリア" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="aebbb-106">The **ClearMacroError** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="aebbb-107">注釈</span><span class="sxs-lookup"><span data-stu-id="aebbb-107">Remarks</span></span>

- <span data-ttu-id="aebbb-108">マクロでエラーが発生すると、エラーに関する情報が **MacroError** オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="aebbb-108">When an error occurs in a macro, information about the error is stored in the **MacroError** object.</span></span> <span data-ttu-id="aebbb-109">" **[OnError](onerror-macro-action.md)** /エラー時" アクションを使用してエラーメッセージが表示されないようにしていない場合は、マクロが停止し、エラー情報が標準的なエラーメッセージに表示されます。</span><span class="sxs-lookup"><span data-stu-id="aebbb-109">If you have not used the **[OnError](onerror-macro-action.md)** action to suppress error messages, the macro stops and the error information is displayed in a standard error message.</span></span> <span data-ttu-id="aebbb-110">ただし、" **OnError** /エラー時" アクションを使用してエラーメッセージが表示されないようにした場合は、 **MacroError**オブジェクトに格納されている情報を条件またはカスタムエラーメッセージで使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="aebbb-110">However, if you have used the **OnError** action to suppress error messages, you might want to use the information stored in the **MacroError** object in a condition or in a custom error message.</span></span>
    
  <span data-ttu-id="aebbb-p102">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action. Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments. This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span><span class="sxs-lookup"><span data-stu-id="aebbb-p102">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action. Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments. This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span></span>

- <span data-ttu-id="aebbb-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span><span class="sxs-lookup"><span data-stu-id="aebbb-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span></span>

- <span data-ttu-id="aebbb-p103">**MacroError** オブジェクトには、一度に 1 つのエラー情報のみが格納されます。マクロで複数のエラーが発生した場合は、最後のエラーに関する情報だけが **MacroError** オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="aebbb-p103">The **MacroError** object contains information about only one error at a time. If more than one error has occurred in a macro, the **MacroError** object contains information only about the last error.</span></span>

- <span data-ttu-id="aebbb-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="aebbb-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="aebbb-118">例</span><span class="sxs-lookup"><span data-stu-id="aebbb-118">Example</span></span>

<span data-ttu-id="aebbb-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span><span class="sxs-lookup"><span data-stu-id="aebbb-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span></span> <span data-ttu-id="aebbb-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span><span class="sxs-lookup"><span data-stu-id="aebbb-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span></span> <span data-ttu-id="aebbb-121">条件\*\* \[MacroError\]。\[0\]\<\>を指定\*\*すると、 **MacroError**オブジェクトがテストされます。</span><span class="sxs-lookup"><span data-stu-id="aebbb-121">The condition **\[MacroError\].\[Number\]\<\>0** tests the **MacroError** object.</span></span> <span data-ttu-id="aebbb-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span><span class="sxs-lookup"><span data-stu-id="aebbb-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span></span> <span data-ttu-id="aebbb-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span><span class="sxs-lookup"><span data-stu-id="aebbb-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span></span> <span data-ttu-id="aebbb-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span><span class="sxs-lookup"><span data-stu-id="aebbb-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aebbb-125">条件</span><span class="sxs-lookup"><span data-stu-id="aebbb-125">Condition</span></span></p></th>
<th><p><span data-ttu-id="aebbb-126">アクション</span><span class="sxs-lookup"><span data-stu-id="aebbb-126">Action</span></span></p></th>
<th><p><span data-ttu-id="aebbb-127">引数</span><span class="sxs-lookup"><span data-stu-id="aebbb-127">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="aebbb-128"><strong>OnError</strong></span><span class="sxs-lookup"><span data-stu-id="aebbb-128"><strong>OnError</strong></span></span></p></td>
<td><p><span data-ttu-id="aebbb-129"><strong>[次へ] に移動し</strong>ます。 <strong></strong></span><span class="sxs-lookup"><span data-stu-id="aebbb-129"><strong>Go to</strong>: <strong>Next</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="aebbb-130"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="aebbb-130"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="aebbb-131"><strong>フォーム名</strong>: カテゴリフォーム<strong>ビュー</strong>: <strong>formwindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="aebbb-131"><strong>Form Name</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="aebbb-132"><strong>GoToRecord</strong></span><span class="sxs-lookup"><span data-stu-id="aebbb-132"><strong>GoToRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="aebbb-133"><strong>オブジェクトの種類</strong>: <strong>formoboffname</strong>: カテゴリフォーム<strong>レコード</strong>: 以前</span><span class="sxs-lookup"><span data-stu-id="aebbb-133"><strong>Object Type</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aebbb-134">[MacroError]。件数&lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="aebbb-134">[MacroError].[Number]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="aebbb-135"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="aebbb-135"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="aebbb-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].件数&amp; &quot; [ &quot; MacroError] &amp;ActionName&amp; &quot;アクション。&quot;<strong>警告音</strong>: <strong>yestype</strong>: 情報</span><span class="sxs-lookup"><span data-stu-id="aebbb-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].[Number] &amp; &quot; on &quot; &amp; [MacroError].[ActionName] &amp; &quot; action.&quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="aebbb-137"><strong>ClearMacroError</strong></span><span class="sxs-lookup"><span data-stu-id="aebbb-137"><strong>ClearMacroError</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

