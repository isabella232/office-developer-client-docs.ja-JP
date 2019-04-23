---
title: MinimizeWindow マクロ アクション
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9f7c4ab535010dc0329673fd04721615f6eb3cd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288884"
---
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="a6079-102">MinimizeWindow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a6079-102">MinimizeWindow macro action</span></span>

<span data-ttu-id="a6079-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6079-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6079-104">タブ付きドキュメントを使用せずにウィンドウを重ねて使用するように Access が構成されている場合、" **MinimizeWindow/ウィンドウの最小化** " アクションを使用してアクティブ ウィンドウを縮小し、Access ウィンドウの下部に小さなタイトル バーとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a6079-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>

> [!NOTE]
> <span data-ttu-id="a6079-p101">[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 **WindowState** プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6079-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="a6079-107">Setting</span><span class="sxs-lookup"><span data-stu-id="a6079-107">Setting</span></span>

<span data-ttu-id="a6079-108">"MinimizeWindow/ウィンドウの最小化" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="a6079-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6079-109">注釈</span><span class="sxs-lookup"><span data-stu-id="a6079-109">Remarks</span></span>

<span data-ttu-id="a6079-p102">You can use this action to remove a window from the screen while leaving the object open. You can also use this action to open an object without displaying its window. To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action. The **RestoreWindow** action restores a minimized window to its previous size.</span><span class="sxs-lookup"><span data-stu-id="a6079-p102">You can use this action to remove a window from the screen while leaving the object open. You can also use this action to open an object without displaying its window. To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action. The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="a6079-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span><span class="sxs-lookup"><span data-stu-id="a6079-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="a6079-115">**ヒント**</span><span class="sxs-lookup"><span data-stu-id="a6079-115">**Tips**</span></span>

- <span data-ttu-id="a6079-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span><span class="sxs-lookup"><span data-stu-id="a6079-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

- <span data-ttu-id="a6079-p103">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.</span><span class="sxs-lookup"><span data-stu-id="a6079-p103">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.</span></span>

- <span data-ttu-id="a6079-p104">アクティブ ウィンドウを非表示にするには、[ **表示**] メニューの [ **このウィンドウの管理**] をクリックし、[ **表示しない**] をクリックします。この場合、ウィンドウは最小化されるのではなく、非表示になります。同じく [ **表示**] メニューの [ **再表示**] をクリックすると、ウィンドウを再度表示できます。これらのコマンドをマクロから実行するには、"RunMenuCommand/メニューコマンドの実行" アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6079-p104">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**. Instead of being reduced to an icon, the window becomes invisible. Use the **Unhide** command on the same menu to make the window reappear. You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

- <span data-ttu-id="a6079-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span><span class="sxs-lookup"><span data-stu-id="a6079-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="a6079-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="a6079-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

