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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715950"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="a629c-102">MaximizeWindow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a629c-102">MaximizeWindow macro action</span></span>

<span data-ttu-id="a629c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a629c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a629c-104">タブ付きドキュメントではなく重ねて表示されるウィンドウを使用するアクセスを構成する場合は、Access ウィンドウ全体に表示されるので、作業中のウィンドウを拡大する**MaximizeWindow**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a629c-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="a629c-105">このアクションを使用すると、アクティブ ウィンドウ内でのオブジェクトの表示範囲を拡大できます。</span><span class="sxs-lookup"><span data-stu-id="a629c-105">This action will allow you to see as much of the object in the active window as possible.</span></span>

> [!NOTE]
> <span data-ttu-id="a629c-p102">[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 **WindowState** プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a629c-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="a629c-108">設定値</span><span class="sxs-lookup"><span data-stu-id="a629c-108">Setting</span></span>

<span data-ttu-id="a629c-109">**MaximizeWindow**アクション引数はありません。</span><span class="sxs-lookup"><span data-stu-id="a629c-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="a629c-110">解説</span><span class="sxs-lookup"><span data-stu-id="a629c-110">Remarks</span></span>

<span data-ttu-id="a629c-111">このアクションは、ウィンドウの右上隅の [**最大化**] ボタンをクリックするか、[**コントロール**] メニューのウィンドウの**最大化**をクリックすると同じです。</span><span class="sxs-lookup"><span data-stu-id="a629c-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="a629c-112">**RestoreWindow**アクションを使用すると、元のサイズを最大化したウィンドウを復元します。</span><span class="sxs-lookup"><span data-stu-id="a629c-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

> [!TIP]
> - <span data-ttu-id="a629c-113">アクティブ ウィンドウ以外のウィンドウを最大化したい場合は、 **SelectObject**アクションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a629c-113">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>
> - <span data-ttu-id="a629c-114">Access で 1 つのウィンドウを最大化すると、その他のウィンドウを開くときやその他のウィンドウに切り替えたときにも、それらのウィンドウはすべて最大化されます。</span><span class="sxs-lookup"><span data-stu-id="a629c-114">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them.</span></span> <span data-ttu-id="a629c-115">ただし、ポップアップ フォームは最大化されません。</span><span class="sxs-lookup"><span data-stu-id="a629c-115">However, pop-up forms aren't maximized.</span></span> <span data-ttu-id="a629c-116">他のウィンドウが最大化されたときにそのサイズを維持するためにフォームを実行する場合に、 **[はい]** に、[ **PopUp** ] プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a629c-116">If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="a629c-117">モジュールの Visual Basic for Applications の**MaximizeWindow**アクションを実行するには、 **DoCmd**オブジェクトの**最大化**の方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="a629c-117">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

