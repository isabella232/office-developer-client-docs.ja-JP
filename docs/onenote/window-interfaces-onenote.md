---
title: ウィンドウ インターフェイス (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: WindowとWindowsのインターフェイスは、 OneNote 2013 API は OneNote ウィンドウを操作するユーザーを有効にするオブジェクトです。これらのオブジェクトでは、OneNote ウィンドウの集合を列挙し、特定のウィンドウのプロパティを変更することができます。
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317037"
---
# <a name="window-interfaces-onenote"></a><span data-ttu-id="1845c-104">ウィンドウ インターフェイス (OneNote 2013)</span><span class="sxs-lookup"><span data-stu-id="1845c-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="1845c-p102">**Window**と **Windows**のインターフェイスは、 OneNote 2013 API は OneNote ウィンドウを操作するユーザーを有効にするオブジェクトです。これらのオブジェクトでは、OneNote ウィンドウの集合を列挙し、特定のウィンドウのプロパティを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="1845c-p102">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows. These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="1845c-107">OneNote ウィンドウ ビュー</span><span class="sxs-lookup"><span data-stu-id="1845c-107">OneNote window views</span></span>

<span data-ttu-id="1845c-108">OneNote ウィンドウ用に使用できる 4 つの表示モードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="1845c-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="1845c-109">通常のビュー： ノートブックとページのナビゲーション ウィンドウに表示されている既定の OneNote ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1845c-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="1845c-110">完全なページの表示： 最小ユーザー インターフェイス (UI) であり、ノートブック、およびページのペインが表示されていないビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1845c-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="1845c-p103">クイック注： 短いメモを取ることができます小さなウィンドウが表示されます。通常、Windows の通知領域に OneNote のアイコンをクイック ノートにアクセスするとは、OneNote の [ **表示**] タブからアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1845c-p103">Quick note—Displays a small window that allows users to take short notes. You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="1845c-p104">デスクトップの端に-(タスク バーのような)、デスクトップの任意の辺に OneNote ウィンドウをドッキングすることができますが表示されます。このビューは、ウィンドウに収まるように、デスクトップのサイズを縮小します。1 つだけのウィンドウをドッキングするには、任意の時点と、ウィンドウは、デスクトップをブロックすることがなく常に表示します。</span><span class="sxs-lookup"><span data-stu-id="1845c-p104">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar). This view reduces the size of the desktop to fit the window. You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="1845c-116">次の図は、完全なページビュー、デスクトップ上のドッキング、およびデスクトップ上のクイックノートの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="1845c-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="1845c-117">**OneNote のビュー**</span><span class="sxs-lookup"><span data-stu-id="1845c-117">**OneNote views**</span></span>

<span data-ttu-id="1845c-118">![OneNote ウィンドウビュー](media/ON15Con_views.jpg "OneNote ウィンドウビュー")</span><span class="sxs-lookup"><span data-stu-id="1845c-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="1845c-119">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1845c-119">Interfaces</span></span>

<span data-ttu-id="1845c-120">このセクションは OneNote ウィンドウをプログラムで変更するのに使用できるメンバー、インターフェイスを示します。</span><span class="sxs-lookup"><span data-stu-id="1845c-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="1845c-121">Windows インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1845c-121">Windows interface</span></span>

<span data-ttu-id="1845c-p105">**Windows**インターフェイスは、一連の OneNote ウィンドウを開いてアクセスすることができます。 **Application.Windows**を使用してアクセス、OneNote の **Application**クラスのプロパティです。これは、OneNote ウィンドウの列挙型のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="1845c-p105">The **Windows** interface allows the user to access the set of opened OneNote windows. It is a property of the OneNote **Application** class, accessed through **Application.Windows**. This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="1845c-125">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="1845c-125">**Properties**</span></span>

|<span data-ttu-id="1845c-126">**名前**</span><span class="sxs-lookup"><span data-stu-id="1845c-126">**Name**</span></span>|<span data-ttu-id="1845c-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="1845c-127">**Type**</span></span>|<span data-ttu-id="1845c-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="1845c-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1845c-129">**Count**</span><span class="sxs-lookup"><span data-stu-id="1845c-129">**Count**</span></span> <br/> |<span data-ttu-id="1845c-130">ulong</span><span class="sxs-lookup"><span data-stu-id="1845c-130">ulong</span></span>  <br/> |<span data-ttu-id="1845c-131">**Windows**セットには、 **Window**オブジェクトの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="1845c-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="1845c-132">**currentwindow**</span><span class="sxs-lookup"><span data-stu-id="1845c-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="1845c-133">**Window**</span><span class="sxs-lookup"><span data-stu-id="1845c-133">**Window**</span></span> <br/> |<span data-ttu-id="1845c-134">アクティブな OneNote ウィンドウの **Window**オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="1845c-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1845c-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="1845c-135">**Items**</span></span> <br/> |<span data-ttu-id="1845c-136">**Window**</span><span class="sxs-lookup"><span data-stu-id="1845c-136">**Window**</span></span> <br/> |<span data-ttu-id="1845c-p106">渡されたインデックス値に対応する **Window**オブジェクトを返します。このプロパティに直接アクセスできません。オブジェクトを返すため、 **Window** 、 **Windows [(uint) index]** を使用します。 </span><span class="sxs-lookup"><span data-stu-id="1845c-p106">Returns the **Window** object that corresponds to the index value passed. This property cannot be accessed directly. To return a **Window** object, use **Windows [(uint) index]**.  </span></span><br/> |
   
### <a name="window-interface"></a><span data-ttu-id="1845c-140">ウィンドウインターフェイス</span><span class="sxs-lookup"><span data-stu-id="1845c-140">Window interface</span></span>

<span data-ttu-id="1845c-p107">**Window**インターフェイスは、各ウィンドウの特定のプロパティにアクセスすることができます。各 OneNote ウィンドウを列挙、 **Application**クラスの **Windows**プロパティを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="1845c-p107">The **Window** interface allows the user to access certain properties of each window. Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="1845c-143">**新しいプロパティ**</span><span class="sxs-lookup"><span data-stu-id="1845c-143">**Properties**</span></span>

|<span data-ttu-id="1845c-144">**名前**</span><span class="sxs-lookup"><span data-stu-id="1845c-144">**Name**</span></span>|<span data-ttu-id="1845c-145">**Type**</span><span class="sxs-lookup"><span data-stu-id="1845c-145">**Type**</span></span>|<span data-ttu-id="1845c-146">**説明**</span><span class="sxs-lookup"><span data-stu-id="1845c-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1845c-147">**Active**</span><span class="sxs-lookup"><span data-stu-id="1845c-147">**Active**</span></span> <br/> |<span data-ttu-id="1845c-148">bool</span><span class="sxs-lookup"><span data-stu-id="1845c-148">bool</span></span>  <br/> |<span data-ttu-id="1845c-149">取得またはウィンドウは、アクティブな OneNote ウィンドウであるかどうかを示す値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1845c-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1845c-150">**Application**</span><span class="sxs-lookup"><span data-stu-id="1845c-150">**Application**</span></span> <br/> |<span data-ttu-id="1845c-151">**アプリケーション**</span><span class="sxs-lookup"><span data-stu-id="1845c-151">**Application**</span></span> <br/> |<span data-ttu-id="1845c-152">ウィンドウに関連付けられている、OneNote の **Application**オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="1845c-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="1845c-153">**CurrentPageId**</span><span class="sxs-lookup"><span data-stu-id="1845c-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="1845c-154">string</span><span class="sxs-lookup"><span data-stu-id="1845c-154">string</span></span>  <br/> |<span data-ttu-id="1845c-155">ウィンドウの作業中の OneNote のページのオブジェクト ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1845c-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="1845c-156">**currentsectionid**</span><span class="sxs-lookup"><span data-stu-id="1845c-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="1845c-157">string</span><span class="sxs-lookup"><span data-stu-id="1845c-157">string</span></span>  <br/> |<span data-ttu-id="1845c-158">ウィンドウの作業中の OneNote のセクションのオブジェクト ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1845c-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="1845c-159">**currentsectiongroupid**</span><span class="sxs-lookup"><span data-stu-id="1845c-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="1845c-160">string</span><span class="sxs-lookup"><span data-stu-id="1845c-160">string</span></span>  <br/> |<span data-ttu-id="1845c-161">オブジェクト ウィンドウの作業中の OneNote のセクション グループの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1845c-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="1845c-162">**CurrentNotebookId**</span><span class="sxs-lookup"><span data-stu-id="1845c-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="1845c-163">string</span><span class="sxs-lookup"><span data-stu-id="1845c-163">string</span></span>  <br/> |<span data-ttu-id="1845c-164">ウィンドウの作業中の OneNote ノートブックのオブジェクト ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1845c-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="1845c-165">**doc/場所**</span><span class="sxs-lookup"><span data-stu-id="1845c-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="1845c-166">**doc/場所**</span><span class="sxs-lookup"><span data-stu-id="1845c-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="1845c-167">取得または、OneNote ウィンドウのドッキング場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="1845c-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1845c-168">**FullPageView**</span><span class="sxs-lookup"><span data-stu-id="1845c-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="1845c-169">bool</span><span class="sxs-lookup"><span data-stu-id="1845c-169">bool</span></span>  <br/> |<span data-ttu-id="1845c-170">取得またはウィンドウが全体表示 (最小限の UI ビュー) であるかどうかを示す値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1845c-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="1845c-171">**sidenote 示す**</span><span class="sxs-lookup"><span data-stu-id="1845c-171">**SideNote**</span></span> <br/> |<span data-ttu-id="1845c-172">bool</span><span class="sxs-lookup"><span data-stu-id="1845c-172">bool</span></span>  <br/> |<span data-ttu-id="1845c-173">取得またはをすばやくメモ ウィンドウだかどうかを示す値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1845c-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="1845c-174">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="1845c-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="1845c-175">ulong</span><span class="sxs-lookup"><span data-stu-id="1845c-175">ulong</span></span>  <br/> |<span data-ttu-id="1845c-176">OneNote ウィンドウのハンドル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1845c-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="1845c-177">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="1845c-177">**Methods**</span></span>
  
<span data-ttu-id="1845c-178">**Window**インターフェイスは、次の方法を使用するには、OneNote ウィンドウに指定したオブジェクトまたは指定した Url に移動します。</span><span class="sxs-lookup"><span data-stu-id="1845c-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="1845c-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="1845c-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1845c-180">**説明**</span><span class="sxs-lookup"><span data-stu-id="1845c-180">**Description**</span></span> <br/> |<span data-ttu-id="1845c-p108">OneNote ウィンドウの指定したオブジェクトに移動します。たとえば、セクション、ページ、およびページ内の要素のアウトラインに移動できます。</span><span class="sxs-lookup"><span data-stu-id="1845c-p108">Navigates to the specified object in the OneNote window. For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="1845c-183">**構文**</span><span class="sxs-lookup"><span data-stu-id="1845c-183">**Syntax**</span></span> <br/> | <span data-ttu-id="1845c-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="1845c-184"></span></span> <br/> |
|<span data-ttu-id="1845c-185">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="1845c-185">**Parameters**</span></span> <br/> | <span data-ttu-id="1845c-p109">_bstrHierarchyObjectID_： に移動するオブジェクトの ID を OneNote の階層です。OneNote のノートブック、セクション、セクション グループ、またはページのオブジェクト ID を参照できます。 </span><span class="sxs-lookup"><span data-stu-id="1845c-p109">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to. The object ID can reference a OneNote notebook, section, section group, or page.  </span></span><br/>  <span data-ttu-id="1845c-p110">_bstrObjectID_-OneNote の ID、特定のオブジェクトを OneNote のページ内に移動します。このパラメーターが設定されているユーザーがいない場合、ページ上の特定のオブジェクトに移動する、null にします。 </span><span class="sxs-lookup"><span data-stu-id="1845c-p110">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page. If the user does not want to navigate to a specific object on a page, this parameter is set to null.  </span></span><br/> |
   
<span data-ttu-id="1845c-190">**NavigateToUrl**</span><span class="sxs-lookup"><span data-stu-id="1845c-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1845c-191">**説明**</span><span class="sxs-lookup"><span data-stu-id="1845c-191">**Description**</span></span> <br/> |<span data-ttu-id="1845c-192">OneNote のリンクを渡された場合 (onenote://)、OneNote 内の対応する場所には、OneNote ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="1845c-192">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote.</span></span> <span data-ttu-id="1845c-193">ただし、リンクが https://や file://などの外部リンクの場合は、[セキュリティ] ダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1845c-193">However, if the link is an external link, such as https:// or file://, a security dialog box will appear.</span></span> <span data-ttu-id="1845c-194">棄却に関する、OneNote でリンクを開くしようし、HResult.hrObjectDoesNotExist エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="1845c-194">Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="1845c-195">**構文**</span><span class="sxs-lookup"><span data-stu-id="1845c-195">**Syntax**</span></span> <br/> | <span data-ttu-id="1845c-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="1845c-196"></span></span> <br/> |
|<span data-ttu-id="1845c-197">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="1845c-197">**Parameters**</span></span> <br/> | <span data-ttu-id="1845c-198">_bstrUrl_-URL に移動します。</span><span class="sxs-lookup"><span data-stu-id="1845c-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="1845c-199">**setdoc/location**</span><span class="sxs-lookup"><span data-stu-id="1845c-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1845c-200">**説明**</span><span class="sxs-lookup"><span data-stu-id="1845c-200">**Description**</span></span> <br/> |<span data-ttu-id="1845c-201">**dockLocation**と **ptMonitor**で、モニターで指定された場所にウィンドウをドッキングします。</span><span class="sxs-lookup"><span data-stu-id="1845c-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="1845c-202">**構文**</span><span class="sxs-lookup"><span data-stu-id="1845c-202">**Syntax**</span></span> <br/> | <span data-ttu-id="1845c-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="1845c-203"></span></span> <br/> |
|<span data-ttu-id="1845c-204">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="1845c-204">**Parameters**</span></span> <br/> | <span data-ttu-id="1845c-205">_dockLocation_ - は、 OneNote 2013ウィンドウのドッキング場所を示します。</span><span class="sxs-lookup"><span data-stu-id="1845c-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="1845c-206">_ptMonitor_ - x、y 座標、ウィンドウを監視する (省略可) を示しますに固定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1845c-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="1845c-207">例</span><span class="sxs-lookup"><span data-stu-id="1845c-207">Example</span></span>

<span data-ttu-id="1845c-p112">次のコードでは、OneNote ウィンドウ ドッキング ウィンドウを反復処理します。ドッキング モードのウィンドウが存在しない場合の例は、作業中のウィンドウをドッキングします。アクティブなウィンドウが存在しない場合、コードは新しいドッキング ウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="1845c-p112">The following code iterates through the OneNote windows to find a docked window. If no docked window exists, the example docks the active window. If no active window exists, the code creates a new docked window.</span></span>
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="1845c-211">関連項目</span><span class="sxs-lookup"><span data-stu-id="1845c-211">See also</span></span>

- [<span data-ttu-id="1845c-212">OneNote の開発者用リファレンス</span><span class="sxs-lookup"><span data-stu-id="1845c-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

