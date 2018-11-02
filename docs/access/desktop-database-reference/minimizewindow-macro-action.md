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
ms.openlocfilehash: 50716a32d0fa3837f87d9d2c5ecde0b59696480d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920369"
---
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="fa087-102">MinimizeWindow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="fa087-102">MinimizeWindow macro action</span></span>


<span data-ttu-id="fa087-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fa087-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa087-104">タブ付きドキュメントを使用せずにウィンドウを重ねて使用するように Access が構成されている場合、" **MinimizeWindow/ウィンドウの最小化** " アクションを使用してアクティブ ウィンドウを縮小し、Access ウィンドウの下部に小さなタイトル バーとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="fa087-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fa087-p101">[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 <STRONG>WindowState</STRONG> プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa087-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="fa087-107">設定値</span><span class="sxs-lookup"><span data-stu-id="fa087-107">Setting</span></span>

<span data-ttu-id="fa087-108">**MinimizeWindow**アクション引数はありません。</span><span class="sxs-lookup"><span data-stu-id="fa087-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa087-109">解説</span><span class="sxs-lookup"><span data-stu-id="fa087-109">Remarks</span></span>

<span data-ttu-id="fa087-110">オブジェクトを開いたまま、ウィンドウを画面から削除するのには、このアクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa087-110">You can use this action to remove a window from the screen while leaving the object open.</span></span> <span data-ttu-id="fa087-111">オブジェクトを開くウィンドウを表示せずにこの操作を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="fa087-111">You can also use this action to open an object without displaying its window.</span></span> <span data-ttu-id="fa087-112">オブジェクトを表示するには、 **MaximizeWindow**または**RestoreWindow**のいずれかのアクションに**SelectObject**アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa087-112">To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action.</span></span> <span data-ttu-id="fa087-113">**RestoreWindow**アクションは、元のサイズを最小化したウィンドウを復元します。</span><span class="sxs-lookup"><span data-stu-id="fa087-113">The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="fa087-114">**MinimizeWindow**アクションは、ウィンドウの右上隅の [**最小化**] ボタンをクリックするか、**コントロール**] メニューの [**最小化**] をクリックと同じです。</span><span class="sxs-lookup"><span data-stu-id="fa087-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="fa087-115">**ヒント**</span><span class="sxs-lookup"><span data-stu-id="fa087-115">**Tips**</span></span>

  - <span data-ttu-id="fa087-116">最初必要があります作業中のウィンドウ以外のウィンドウを最小化したい場合は、 **SelectObject**アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa087-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

  - <span data-ttu-id="fa087-117">ナビゲーション ウィンドウを非表示にするには、ナビゲーション ウィンドウに引数が **[はい]** に設定し、 **MinimizeWindow**アクションを使用して**SelectObject**アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa087-117">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action.</span></span> <span data-ttu-id="fa087-118">**SelectObject**アクションで選択したオブジェクトは、データベース内のオブジェクトにできます。</span><span class="sxs-lookup"><span data-stu-id="fa087-118">The object you select in the **SelectObject** action can be any object in the database.</span></span>

  - <span data-ttu-id="fa087-p104">アクティブ ウィンドウを非表示にするには、[ **表示**] メニューの [ **このウィンドウの管理**] をクリックし、[ **表示しない**] をクリックします。この場合、ウィンドウは最小化されるのではなく、非表示になります。同じく [ **表示**] メニューの [ **再表示**] をクリックすると、ウィンドウを再度表示できます。これらのコマンドをマクロから実行するには、"RunMenuCommand/メニューコマンドの実行" アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa087-p104">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**. Instead of being reduced to an icon, the window becomes invisible. Use the **Unhide** command on the same menu to make the window reappear. You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

  - <span data-ttu-id="fa087-123">フォームのウィンドウを表示または非表示に、フォームの**Visible**プロパティを設定するのには **、アクション**を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="fa087-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="fa087-124">Visual Basic for Applications (VBA) モジュールに**MinimizeWindow**アクションを実行するには、 **DoCmd**オブジェクトの**最小化**の方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="fa087-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

