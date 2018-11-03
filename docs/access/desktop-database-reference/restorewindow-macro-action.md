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
ms.openlocfilehash: fb857e7eda7860150feb7af07babcc2574c3972f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929049"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="ab435-102">RestoreWindow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="ab435-102">RestoreWindow macro action</span></span>


<span data-ttu-id="ab435-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ab435-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab435-104">**RestoreWindow**アクションを使用すると、元のサイズを最大化または最小化されたウィンドウを復元します。</span><span class="sxs-lookup"><span data-stu-id="ab435-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ab435-p101">[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 <STRONG>WindowState</STRONG> プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab435-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="ab435-107">設定値</span><span class="sxs-lookup"><span data-stu-id="ab435-107">Setting</span></span>

<span data-ttu-id="ab435-108">**RestoreWindow**アクション引数はありません。</span><span class="sxs-lookup"><span data-stu-id="ab435-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab435-109">解説</span><span class="sxs-lookup"><span data-stu-id="ab435-109">Remarks</span></span>

<span data-ttu-id="ab435-110">この操作は、選択したオブジェクトに対して機能します。</span><span class="sxs-lookup"><span data-stu-id="ab435-110">This action works on the selected object.</span></span> <span data-ttu-id="ab435-111">オブジェクトが最小化されている場合、 **SelectObject**アクションを使用して選択して、 **RestoreWindow**アクションを使用して元のサイズに復元できます。</span><span class="sxs-lookup"><span data-stu-id="ab435-111">If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="ab435-112">移動または復元したウィンドウのサイズは、 **MoveAndSizeWindow**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab435-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="ab435-113">**RestoreWindow**アクションは、ウィンドウの右上隅で [**復元**] ボタンをクリックするか、ウィンドウの**コントロール**メニューの [**復元**] コマンドをクリックすると同じです。</span><span class="sxs-lookup"><span data-stu-id="ab435-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="ab435-114">Visual Basic for Applications (VBA) モジュールに**RestoreWindow**アクションを実行するには、 **DoCmd**オブジェクトの**復元**方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab435-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

