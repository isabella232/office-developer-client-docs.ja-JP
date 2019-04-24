---
title: RestoreWindow マクロ アクション
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306588"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="01bef-102">RestoreWindow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="01bef-102">RestoreWindow macro action</span></span>

<span data-ttu-id="01bef-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="01bef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01bef-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span><span class="sxs-lookup"><span data-stu-id="01bef-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>

> [!NOTE]
> <span data-ttu-id="01bef-p101">[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 **WindowState** プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="01bef-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="01bef-107">Setting</span><span class="sxs-lookup"><span data-stu-id="01bef-107">Setting</span></span>

<span data-ttu-id="01bef-108">"RestoreWindow/ウィンドウを元のサイズに戻す" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="01bef-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="01bef-109">注釈</span><span class="sxs-lookup"><span data-stu-id="01bef-109">Remarks</span></span>

<span data-ttu-id="01bef-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span><span class="sxs-lookup"><span data-stu-id="01bef-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="01bef-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span><span class="sxs-lookup"><span data-stu-id="01bef-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="01bef-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span><span class="sxs-lookup"><span data-stu-id="01bef-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="01bef-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="01bef-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

