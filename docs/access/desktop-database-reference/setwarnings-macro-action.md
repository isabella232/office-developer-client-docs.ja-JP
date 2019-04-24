---
title: SetWarnings マクロ アクション
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308660"
---
# <a name="setwarnings-macro-action"></a><span data-ttu-id="b042d-102">SetWarnings マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b042d-102">SetWarnings macro action</span></span>

<span data-ttu-id="b042d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b042d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b042d-104">You can use the **SetWarnings** action to turn system messages on or off.</span><span class="sxs-lookup"><span data-stu-id="b042d-104">You can use the **SetWarnings** action to turn system messages on or off.</span></span>

> [!NOTE]
> <span data-ttu-id="b042d-105">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="b042d-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b042d-106">設定値</span><span class="sxs-lookup"><span data-stu-id="b042d-106">Setting</span></span>

<span data-ttu-id="b042d-107">"SetWarnings/メッセージの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b042d-107">The **SetWarnings** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b042d-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="b042d-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b042d-109">説明</span><span class="sxs-lookup"><span data-stu-id="b042d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b042d-110"><strong>Warnings On/メッセージの表示</strong></span><span class="sxs-lookup"><span data-stu-id="b042d-110"><strong>Warnings On</strong></span></span></p></td>
<td><p><span data-ttu-id="b042d-p101">システム メッセージを表示するかどうかを指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] にある [<strong>メッセージの表示</strong>] ボックスで、システム メッセージを表示する場合は [<strong>はい</strong>]、システム メッセージを表示しない場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>いいえ</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="b042d-p101">Specifies whether system messages are displayed. Click <strong>Yes</strong> (to turn on system messages) or <strong>No</strong> (to turn off system messages) in the <strong>Warnings On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b042d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b042d-114">Remarks</span></span>

<span data-ttu-id="b042d-p102">このアクションを使用すると、モーダルな通知やメッセージ ボックスによってマクロが停止しないようにすることができます。ただし、エラー メッセージは常に表示されます。また、[ **OK**]、[ **キャンセル**]、[ **はい**]、[ **いいえ**] などのボタンをクリックする以外に、テキストの入力やオプションの選択を必要とするダイアログ ボックスも表示されます。</span><span class="sxs-lookup"><span data-stu-id="b042d-p102">You can use this action to prevent modal warnings and message boxes from stopping the macro. However, error messages are always displayed. Also, Microsoft Access displays any dialog boxes that require input other than just choosing a button (such as **OK**, **Cancel**, **Yes**, or **No**) — for example, any dialog box that requires you to enter text or select one of several options.</span></span>

<span data-ttu-id="b042d-p103">"Warnings On/メッセージの表示" 引数を [ **いいえ**] に設定してこのアクションを実行すると、通知やメッセージ ボックスが表示されたときに **Enter** キーを押した場合と同じ動作になります。通常、通知やメッセージが表示された場合は、[ **OK**] ボタンまたは [ **はい**] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="b042d-p103">Carrying out this action with the **Warnings On** argument set to **No** has the same effect as pressing ENTER whenever a warning or message box is displayed. Typically, an **OK** or **Yes** button is chosen in response to the warning or message.</span></span>

<span data-ttu-id="b042d-120">マクロが完了すると、自動的にシステム メッセージの表示がオンに戻ります。</span><span class="sxs-lookup"><span data-stu-id="b042d-120">When the macro finishes, Access automatically turns the display of system messages back on.</span></span>

<span data-ttu-id="b042d-p104">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished. You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span><span class="sxs-lookup"><span data-stu-id="b042d-p104">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished. You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span></span>

> [!WARNING]
> <span data-ttu-id="b042d-p105">Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off. In some situations, you won't want to continue a macro if a certain warning message is displayed. Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span><span class="sxs-lookup"><span data-stu-id="b042d-p105">Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off. In some situations, you won't want to continue a macro if a certain warning message is displayed. Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span></span>

<span data-ttu-id="b042d-126">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="b042d-126">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span></span>

