---
title: "'ClearMacroError/マクロエラーのクリア' マクロ アクション"
TOCTitle: ClearMacroError Macro Action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8e5cf0b8cb7ac5b9c49e86ae3a0399d0222b3b04
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477308"
---
# <a name="clearmacroerror-macro-action"></a><span data-ttu-id="046ee-102">"ClearMacroError/マクロエラーのクリア" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="046ee-102">ClearMacroError Macro Action</span></span>


<span data-ttu-id="046ee-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="046ee-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="046ee-104">**ClearMacroError**アクションを使用すると、 **MacroError**オブジェクトに格納されているエラーについての情報をクリアします。</span><span class="sxs-lookup"><span data-stu-id="046ee-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span></span>

## <a name="setting"></a><span data-ttu-id="046ee-105">設定値</span><span class="sxs-lookup"><span data-stu-id="046ee-105">Setting</span></span>

<span data-ttu-id="046ee-106">**ClearMacroError**アクションの引数ではありません。</span><span class="sxs-lookup"><span data-stu-id="046ee-106">The **ClearMacroError** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="046ee-107">注釈</span><span class="sxs-lookup"><span data-stu-id="046ee-107">Remarks</span></span>

  - <span data-ttu-id="046ee-108">マクロでエラーが発生すると、エラーに関する情報が **MacroError** オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="046ee-108">When an error occurs in a macro, information about the error is stored in the **MacroError** object.</span></span> <span data-ttu-id="046ee-109">エラー メッセージが表示されないようにするのには、**[エラー時](onerror-macro-action.md)** のアクションを使用しない場合は、マクロが停止し、エラー情報が標準エラー メッセージに表示されます。</span><span class="sxs-lookup"><span data-stu-id="046ee-109">If you have not used the **[OnError](onerror-macro-action.md)** action to suppress error messages, the macro stops and the error information is displayed in a standard error message.</span></span> <span data-ttu-id="046ee-110">ただし、エラー メッセージが表示されないようにするのには、**エラー時**のアクションを使用した場合を条件またはカスタム エラー メッセージでは、 **MacroError**オブジェクトに格納された情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="046ee-110">However, if you have used the **OnError** action to suppress error messages, you might want to use the information stored in the **MacroError** object in a condition or in a custom error message.</span></span>
    
    <span data-ttu-id="046ee-111">エラーが処理された後、 **MacroError**オブジェクト内の情報は古く、 **ClearMacroError**アクションを使用してオブジェクトを消去することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="046ee-111">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action.</span></span> <span data-ttu-id="046ee-112">これにより、 **MacroError**オブジェクトのエラー番号が 0 にリセットし、エラーの説明、マクロ名、アクション名、条件、および引数など、オブジェクトに格納されているエラーに関するその他の情報をクリアします。</span><span class="sxs-lookup"><span data-stu-id="046ee-112">Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments.</span></span> <span data-ttu-id="046ee-113">このようにすると、後で再度 **MacroError** オブジェクトを調査して、別のエラーが発生していないかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="046ee-113">This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span></span>

  - <span data-ttu-id="046ee-114">**ClearMacroError**アクションを使用して、マクロの末尾にする必要はありませんのでは、 **MacroError**オブジェクトが任意のマクロが終了すると自動的にクリアされます。</span><span class="sxs-lookup"><span data-stu-id="046ee-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span></span>

  - <span data-ttu-id="046ee-p103">**MacroError** オブジェクトには、一度に 1 つのエラー情報のみが格納されます。マクロで複数のエラーが発生した場合は、最後のエラーに関する情報だけが **MacroError** オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="046ee-p103">The **MacroError** object contains information about only one error at a time. If more than one error has occurred in a macro, the **MacroError** object contains information only about the last error.</span></span>

  - <span data-ttu-id="046ee-117">**ClearMacroError**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**ClearMacroError**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="046ee-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="046ee-118">使用例</span><span class="sxs-lookup"><span data-stu-id="046ee-118">Example</span></span>

<span data-ttu-id="046ee-119">次のマクロは、**次**の引数**OnError**アクションを使用して、エラー メッセージが表示されないようにし **、このアクション**を使用して、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="046ee-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span></span> <span data-ttu-id="046ee-120">この例では、エラーが意図的に前のレコードに移動するのには、 **GoToRecord**アクションを使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="046ee-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span></span> <span data-ttu-id="046ee-121">条件**\[MacroError\]です\[。数\]\<\>0** 、 **MacroError**オブジェクトをテストします。</span><span class="sxs-lookup"><span data-stu-id="046ee-121">The condition **\[MacroError\].\[Number\]\<\>0** tests the **MacroError** object.</span></span> <span data-ttu-id="046ee-122">エラーが発生した場合、エラー番号は、0 以外の場合、および**メッセージ ボックス**のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="046ee-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span></span> <span data-ttu-id="046ee-123">メッセージ ボックスが表示されます (ここでは、 **GoToRecord**アクション)、エラーを発生させたアクションの名前と、エラー番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="046ee-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span></span> <span data-ttu-id="046ee-124">最後に、 **ClearMacroError**アクションを実行すると、 **MacroError**オブジェクトがクリアされます。</span><span class="sxs-lookup"><span data-stu-id="046ee-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="046ee-125">条件</span><span class="sxs-lookup"><span data-stu-id="046ee-125">Condition</span></span></p></th>
<th><p><span data-ttu-id="046ee-126">アクション</span><span class="sxs-lookup"><span data-stu-id="046ee-126">Action</span></span></p></th>
<th><p><span data-ttu-id="046ee-127">引数</span><span class="sxs-lookup"><span data-stu-id="046ee-127">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="046ee-128"><strong>OnError</strong></span><span class="sxs-lookup"><span data-stu-id="046ee-128"><strong>OnError</strong></span></span></p></td>
<td><p><span data-ttu-id="046ee-129"><strong>移動</strong>:<strong>次へ</strong></span><span class="sxs-lookup"><span data-stu-id="046ee-129"><strong>Go to</strong>: <strong>Next</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="046ee-130"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="046ee-130"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="046ee-131"><strong>フォーム名</strong>: CategoryForm<strong>ビュー</strong>: <strong>FormWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="046ee-131"><strong>Form Name</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="046ee-132"><strong>GoToRecord</strong></span><span class="sxs-lookup"><span data-stu-id="046ee-132"><strong>GoToRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="046ee-133"><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: CategoryForm<strong>レコード</strong>: 前</span><span class="sxs-lookup"><span data-stu-id="046ee-133"><strong>Object Type</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="046ee-134">[MacroError] です。[番号]&lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="046ee-134">[MacroError].[Number]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="046ee-135"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="046ee-135"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="046ee-136"><strong>メッセージ</strong>: =&quot;エラー # &quot; &amp; [MacroError] です。[番号]&amp; &quot; [ &quot; &amp; [MacroError] です。[アクション名]&amp; &quot;アクション。&quot;<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: 情報</span><span class="sxs-lookup"><span data-stu-id="046ee-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].[Number] &amp; &quot; on &quot; &amp; [MacroError].[ActionName] &amp; &quot; action.&quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="046ee-137"><strong>ClearMacroError</strong></span><span class="sxs-lookup"><span data-stu-id="046ee-137"><strong>ClearMacroError</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

