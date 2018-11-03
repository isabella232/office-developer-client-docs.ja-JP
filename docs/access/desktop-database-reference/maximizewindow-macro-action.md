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
ms.openlocfilehash: 452e676d3becb7f5f76587a970b71a42e4ec8ab2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928650"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="57cc6-102">MaximizeWindow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="57cc6-102">MaximizeWindow macro action</span></span>


<span data-ttu-id="57cc6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="57cc6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57cc6-104">タブ付きドキュメントではなく重ねて表示されるウィンドウを使用するアクセスを構成する場合は、Access ウィンドウ全体に表示されるので、作業中のウィンドウを拡大する**MaximizeWindow**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="57cc6-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="57cc6-105">このアクションを使用すると、アクティブ ウィンドウ内でのオブジェクトの表示範囲を拡大できます。</span><span class="sxs-lookup"><span data-stu-id="57cc6-105">This action will allow you to see as much of the object in the active window as possible.</span></span>


> [!NOTE]
> <P><span data-ttu-id="57cc6-p102">[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 <STRONG>WindowState</STRONG> プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="57cc6-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="57cc6-108">設定値</span><span class="sxs-lookup"><span data-stu-id="57cc6-108">Setting</span></span>

<span data-ttu-id="57cc6-109">**MaximizeWindow**アクション引数はありません。</span><span class="sxs-lookup"><span data-stu-id="57cc6-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="57cc6-110">解説</span><span class="sxs-lookup"><span data-stu-id="57cc6-110">Remarks</span></span>

<span data-ttu-id="57cc6-111">このアクションは、ウィンドウの右上隅の [**最大化**] ボタンをクリックするか、[**コントロール**] メニューのウィンドウの**最大化**をクリックすると同じです。</span><span class="sxs-lookup"><span data-stu-id="57cc6-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="57cc6-112">**RestoreWindow**アクションを使用すると、元のサイズを最大化したウィンドウを復元します。</span><span class="sxs-lookup"><span data-stu-id="57cc6-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

<span data-ttu-id="57cc6-113">**ヒント**</span><span class="sxs-lookup"><span data-stu-id="57cc6-113">**Tips**</span></span>

  - <span data-ttu-id="57cc6-114">アクティブ ウィンドウ以外のウィンドウを最大化したい場合は、 **SelectObject**アクションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57cc6-114">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>

  - <span data-ttu-id="57cc6-115">Access で 1 つのウィンドウを最大化すると、その他のウィンドウを開くときやその他のウィンドウに切り替えたときにも、それらのウィンドウはすべて最大化されます。</span><span class="sxs-lookup"><span data-stu-id="57cc6-115">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them.</span></span> <span data-ttu-id="57cc6-116">ただし、ポップアップ フォームは最大化されません。</span><span class="sxs-lookup"><span data-stu-id="57cc6-116">However, pop-up forms aren't maximized.</span></span> <span data-ttu-id="57cc6-117">他のウィンドウが最大化されたときにそのサイズを維持するためにフォームを実行する場合に、 **[はい]** に、[ **PopUp** ] プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="57cc6-117">If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="57cc6-118">モジュールの Visual Basic for Applications の**MaximizeWindow**アクションを実行するには、 **DoCmd**オブジェクトの**最大化**の方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="57cc6-118">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

