---
title: MaximizeWindow マクロ アクション
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289750"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="20149-102">MaximizeWindow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="20149-102">MaximizeWindow macro action</span></span>

<span data-ttu-id="20149-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="20149-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20149-104">タブ付きドキュメントではなく、重なっているウィンドウを使用するように Access が構成されている場合は、[**最大化] ウィンドウ**アクションを使用してアクティブウィンドウを拡大し、access ウィンドウに表示されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="20149-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="20149-105">このアクションを使用すると、アクティブ ウィンドウ内でのオブジェクトの表示範囲を拡大できます。</span><span class="sxs-lookup"><span data-stu-id="20149-105">This action will allow you to see as much of the object in the active window as possible.</span></span>

> [!NOTE]
> <span data-ttu-id="20149-p102">[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 **WindowState** プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="20149-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="20149-108">Setting</span><span class="sxs-lookup"><span data-stu-id="20149-108">Setting</span></span>

<span data-ttu-id="20149-109">"MaximizeWindow/ウィンドウの最大化" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="20149-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="20149-110">注釈</span><span class="sxs-lookup"><span data-stu-id="20149-110">Remarks</span></span>

<span data-ttu-id="20149-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span><span class="sxs-lookup"><span data-stu-id="20149-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="20149-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span><span class="sxs-lookup"><span data-stu-id="20149-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

> [!TIP]
> - <span data-ttu-id="20149-113">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span><span class="sxs-lookup"><span data-stu-id="20149-113">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>
> - <span data-ttu-id="20149-p103">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span><span class="sxs-lookup"><span data-stu-id="20149-p103">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="20149-117">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="20149-117">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

