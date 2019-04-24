---
title: クイック ファイリング ダイアログ ボックス インタ フェース (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: このトピックは、 OneNote 2013では、[クイック ファイリング] ダイアログ ボックスをプログラムでカスタマイズするのに使用できるインターフェイスについて説明します。
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317100"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="6fead-103">クイック ファイリング ダイアログ ボックス インタ フェース (OneNote 2013)</span><span class="sxs-lookup"><span data-stu-id="6fead-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="6fead-104">このトピックは、 OneNote 2013では、[クイック ファイリング] ダイアログ ボックスをプログラムでカスタマイズするのに使用できるインターフェイスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6fead-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="6fead-105">[クイックファイリング] ダイアログボックス</span><span class="sxs-lookup"><span data-stu-id="6fead-105">Quick Filing dialog box</span></span>

<span data-ttu-id="6fead-p101">クイック ファイリング] ダイアログ ボックスのOneNote 2013では、OneNote の階層構造内の場所を選択できるようにするカスタマイズ可能なダイアログ ボックスです。選択可能な場所には、ノートブック、セクション グループ、セクション、ページおよびサブページが含まれます。ダイアログ ボックスは、OneNote アプリケーション内およびOneNote 2013 API を通じて、外部アプリケーションによって使用されます。図 1 は、既定の状態でクイック ファイリング] ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="6fead-p101">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure. Selectable locations include notebooks, section groups, sections, pages, and subpages. The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API. Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="6fead-110">**図 1。クイック ファイリング] ダイアログ ボックスのカスタマイズなし**</span><span class="sxs-lookup"><span data-stu-id="6fead-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="6fead-111">![カスタマイズのない [クイックファイリング] ダイアログボックス](media/ON15Con_quick_filing_dialog.jpg "カスタマイズのない [クイックファイリング] ダイアログボックス")</span><span class="sxs-lookup"><span data-stu-id="6fead-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="6fead-p102">ユーザー、ダイアログ ボックス内の特定の場所、または、テキスト ボックスに入力することによって、OneNote ツリー構造の検索をすべてのノートブックの階層を移動できます。カスタマイズ可能なダイアログ ボックスの側面には、タイトル、説明、最近の結果のリスト、チェック ボックスのテキストと状態、ツリーの深さ、ボタン、および選択可能な場所の種類が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6fead-p102">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box. Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="6fead-p103">クイック ファイリング ダイアログ ボックス機能はOneNote 2013の 2 つのインターフェイスを通じてアクセスできます。 **IQuickFilingDialog**インタ フェースのインスタンスを作成、設定することができます、ダイアログ ボックスを実行する. **IQuickFilingDialogCallback**インターフェイスは、ダイアログ ボックスが閉じられた後に呼び出されます。ダイアログ ボックスは、OneNote のプロセスで実行されるため、ダイアログ ボックスのスレッドの実行を維持する機構が必要にしが閉じているときに、ユーザーの選択やダイアログ ボックスの状態をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="6fead-p103">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces. The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box. The **IQuickFilingDialogCallback** interface is called after the dialog box is closed. The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="6fead-118">iquickfilingdialog インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6fead-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="6fead-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="6fead-119"></span></span>

<span data-ttu-id="6fead-p104">このインターフェイスをカスタマイズして、ダイアログ ボックスを実行することができます。ユーザーは、 **Application.QuickFilingDialog**メソッドを使用して、 **Application**クラスを使用する] ダイアログ ボックスをインスタンス化できます。このメソッドはダイアログ ボックスのインスタンスを返します。 **IQuickFilingDialog.Run**メソッドのプロパティ] ダイアログ ボックスの設定は、ダイアログ ボックスを実行する使用されます。このメソッドは、新しいスレッドで、ダイアログ ボックスを実行します。</span><span class="sxs-lookup"><span data-stu-id="6fead-p104">This interface allows the user to customize and run the dialog box. The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method. The method returns an instance of the dialog box. Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box. This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="6fead-125">**新しいプロパティ**</span><span class="sxs-lookup"><span data-stu-id="6fead-125">**Properties**</span></span>

|<span data-ttu-id="6fead-126">**名前**</span><span class="sxs-lookup"><span data-stu-id="6fead-126">**Name**</span></span>|<span data-ttu-id="6fead-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="6fead-127">**Type**</span></span>|<span data-ttu-id="6fead-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fead-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="6fead-129">**Title**</span></span> <br/> |<span data-ttu-id="6fead-130">string</span><span class="sxs-lookup"><span data-stu-id="6fead-130">string</span></span>  <br/> |<span data-ttu-id="6fead-131">取得またはダイアログ ボックス ウィンドウのタイトル バーに表示されるタイトル テキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="6fead-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="6fead-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="6fead-132">**Description**</span></span> <br/> |<span data-ttu-id="6fead-133">string</span><span class="sxs-lookup"><span data-stu-id="6fead-133">string</span></span>  <br/> |<span data-ttu-id="6fead-p105">取得または設定、テキストの説明に何を選択するように指示します。この値は、複数行のテキストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="6fead-p105">Gets or sets the text description to instruct the user about what to select. This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="6fead-136">**CheckboxText**</span><span class="sxs-lookup"><span data-stu-id="6fead-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="6fead-137">string</span><span class="sxs-lookup"><span data-stu-id="6fead-137">string</span></span>  <br/> |<span data-ttu-id="6fead-p106">取得または、次のチェック ボックスのテキストを設定します。この値が空でない文字列に設定] ダイアログ ボックスで、チェック ボックスが表示されます。値は、空の文字列は、チェック ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="6fead-p106">Gets or sets the text that follows the check box. If this value is set to a non-empty string, a check box appears in the dialog box. If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="6fead-141">**CheckboxState**</span><span class="sxs-lookup"><span data-stu-id="6fead-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="6fead-142">bool</span><span class="sxs-lookup"><span data-stu-id="6fead-142">bool</span></span>  <br/> |<span data-ttu-id="6fead-p107">取得またはチェック ボックスの状態を設定します。 **false**に設定されている場合、ダイアログ ボックスを起動します] チェック ボックスは消去されます。 **true**が指定されている場合、ダイアログ ボックスの **CheckboxText**が空でない文字列が開始されると、このチェック ボックスが選択されます。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p107">Gets or sets the state of the check box. If value is set to **false**, the check box is cleared when the dialog box is started. If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.  </span></span><br/> |
|<span data-ttu-id="6fead-146">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="6fead-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="6fead-147">ulong</span><span class="sxs-lookup"><span data-stu-id="6fead-147">ulong</span></span>  <br/> |<span data-ttu-id="6fead-148">クイック ファイリング ダイアログ ボックス ウィンドウのハンドル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6fead-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="6fead-149">**ツリーの深さ**</span><span class="sxs-lookup"><span data-stu-id="6fead-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="6fead-150">**HierarchyElement**</span><span class="sxs-lookup"><span data-stu-id="6fead-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="6fead-p108">取得または設定、OneNote ツリー深さ、すべてのノートブック セクションに表示されます。既定では最大のセクションでは、ツリーが表示されます。このプロパティは要素の種類を選択することができます。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p108">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section. By default, the tree is displayed up to the sections. This property does not affect what type of elements can be selected.  </span></span><br/> <span data-ttu-id="6fead-p109">**TreeDepth**設定されている場合、要素をボタンのいずれかを選択できますが、OneNote の階層の下位に、表示されているツリーの深さは最も低い可能の選択可能な要素になります。つまり、ツリーの深さは、ページに表示する設定が選択可能な最小の要素は、セクション、セクションにツリーが表示されます。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p109">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element. That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.  </span></span><br/> |
|<span data-ttu-id="6fead-156">**ParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="6fead-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="6fead-157">ulong</span><span class="sxs-lookup"><span data-stu-id="6fead-157">ulong</span></span>  <br/> |<span data-ttu-id="6fead-p110">取得またはダイアログ ボックスの親ウィンドウのハンドル ID を設定します。このプロパティが設定されている場合クイック ファイリング] ダイアログ ボックスになります割り当てられている親ウィンドウをモーダル ダイアログ ボックスを開くと。ユーザーはクイック ファイリング] ダイアログ ボックスが閉じられるまで、親ウィンドウにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6fead-p110">Gets or sets the handle ID of the parent window of the dialog box. If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens. That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="6fead-161">**Position**</span><span class="sxs-lookup"><span data-stu-id="6fead-161">**Position**</span></span> <br/> |<span data-ttu-id="6fead-162">tagpoint</span><span class="sxs-lookup"><span data-stu-id="6fead-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="6fead-p111">取得または、画面を基準にして、[ウィンドウの位置を設定します。既定では親ウィンドウまたはデスクトップの中央に、ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6fead-p111">Gets or sets the position of the window in relation to the screen. By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="6fead-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="6fead-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="6fead-166">string</span><span class="sxs-lookup"><span data-stu-id="6fead-166">string</span></span>  <br/> |<span data-ttu-id="6fead-p112">ダイアログ ボックスを閉じたときに、ユーザーが選択した OneNote の場所のオブジェクト ID を取得します。オブジェクトが設定されている場合は、ユーザーが **[キャンセル**] ボタンをクリックすると、null にします。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p112">Gets the object ID of the OneNote location selected by the user when the dialog box is closed. If the user clicks the **Cancel** button, the object is set to null.  </span></span><br/> |
|<span data-ttu-id="6fead-169">**PressedButton**</span><span class="sxs-lookup"><span data-stu-id="6fead-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="6fead-170">ulong</span><span class="sxs-lookup"><span data-stu-id="6fead-170">ulong</span></span>  <br/> |<span data-ttu-id="6fead-p113">ダイアログ ボックスが閉じるときにクリックしてされたボタンを取得します。 **[キャンセル**] ボタンがクリックしてされた場合は、このプロパティは-1 を返します。他のすべてのボタンがダイアログ ボックスに追加のボタンごとに 1 ずつインクリメントされます、0 から整数値が割り当てられます。既定の **[ok]** ボタンの整数の値は 0 です。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p113">Gets which button was clicked when the dialog box was closed. If the **Cancel** button was clicked, this property returns a value of -1. All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box. The integer value of the default **OK** button is 0.  </span></span><br/> |
   
### <a name="methods"></a><span data-ttu-id="6fead-175">メソッド</span><span class="sxs-lookup"><span data-stu-id="6fead-175">Methods</span></span>

<span data-ttu-id="6fead-176">**SetRecentResults**</span><span class="sxs-lookup"><span data-stu-id="6fead-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-177">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-177">**Description**</span></span> <br/> |<span data-ttu-id="6fead-p114">クイック ファイリング ダイアログ ボックスで、どのような最近の結果のリストが表示されますを設定していくつかの特別なファイリングの場所リストに追加するかどうかを示します。ユーザーは、 [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType)列挙体からの最近の結果リストを選択できます。ユーザーは、次のオプションを一覧に追加する選択もできます。 現在のセクション、現在のページ、または落書きノート。 **RecentResultType.rrtNone**を選択すると、結果の最新のリストは表示されません。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p114">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list. Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration. Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes. If **RecentResultType.rrtNone** is selected, no recent result list is shown.  </span></span><br/> |
|<span data-ttu-id="6fead-182">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="6fead-183">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-183">**Parameters**</span></span> <br/> | <span data-ttu-id="6fead-184">_recentResults_&ndash;最近の結果リストがある場合は、それが表示されることを示す、 **RecentResultType**型のオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6fead-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="6fead-185">**rrtNone**がオンの場合] ダイアログ ボックスで最新の結果のリストは表示されません。</span><span class="sxs-lookup"><span data-stu-id="6fead-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="6fead-186">_fshowcurrentsection_&ndash;最新の結果リストに現在のセクションを含める必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6fead-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="6fead-187">_fShowCurrentPage_&ndash;現在のページを最近の結果リストに含める必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6fead-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="6fead-188">_fShowUnfiledNotes_&ndash; [落書きノート] セクションを最近の結果リストに含めるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6fead-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6fead-p116">[!メモ] 特別なファイリングの場所] ダイアログ ボックスで、ボタンのいずれかで選択できません、する場合、一覧には表示されません。最近の結果の一覧で、選択可能な項目が見つからない場合、結果の最新のリストは表示されません。</span><span class="sxs-lookup"><span data-stu-id="6fead-p116">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list. If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="6fead-191">次の使用例は、最近の結果の一覧で、現在のセクション、現在のページと、落書きノート セクションを表示するのに、 **SetRecentResults**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6fead-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

<span data-ttu-id="6fead-192">**addbutton**</span><span class="sxs-lookup"><span data-stu-id="6fead-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-193">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-193">**Description**</span></span> <br/> |<span data-ttu-id="6fead-p117">ユーザーを追加し、ダイアログ ボックスのボタンをカスタマイズできます。ユーザーは、ボタンと各ボタンで選択できるは、OneNote の階層の要素に、テキストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="6fead-p117">Allows users to add and customize buttons in the dialog box. Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="6fead-196">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="6fead-197">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-197">**Parameters**</span></span> <br/> | <span data-ttu-id="6fead-198">_bstrtext_&ndash;ボタンに表示するテキストを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="6fead-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="6fead-199">既定の **[ok]** ボタンをカスタマイズするには、null 値 **bstrText**として渡します。</span><span class="sxs-lookup"><span data-stu-id="6fead-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="6fead-200">_allowedElements_&ndash;ユーザーがボタンを使用して選択できる、読み取り専用でない OneNote 階層要素を示す**HierarchyElement** 。</span><span class="sxs-lookup"><span data-stu-id="6fead-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="6fead-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="6fead-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="6fead-202">_allowedReadOnlyElements_&ndash;ユーザーがボタンを使用して選択できる OneNote の読み取り専用階層要素を示す**HierarchyElement** 。</span><span class="sxs-lookup"><span data-stu-id="6fead-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="6fead-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="6fead-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="6fead-204">_fdefault_&ndash;このボタンを既定のボタンにするかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6fead-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="6fead-205">複数のボタンを既定値として設定した場合、最後に指定したボタンが既定のボタンになります。</span><span class="sxs-lookup"><span data-stu-id="6fead-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="6fead-p122">次の使用例は、3 つのボタンをクイック ファイリング ダイアログ ボックス。OneNote の階層ツリー内のすべての要素を **すべて**最初のものを選択できます。他、 **ノートブック** **ページ**、ノート パソコンと、ページは、対応する要素が選択されている場合にのみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="6fead-p122">The following example adds three buttons to the Quick Filing dialog box. The first one, **All**, can be selected by all elements in the OneNote hierarchy tree. The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

<span data-ttu-id="6fead-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="6fead-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-210">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-210">**Description**</span></span> <br/> |<span data-ttu-id="6fead-p123">新しいスレッドからクイック ファイリング ダイアログ ボックスが表示されます。ダイアログ ボックスを閉じますを **OnDialogClosed**メソッドが呼び出されます、 **IQuickFilingDialogCallback**インターフェイスへの参照になります。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p123">Displays the Quick Filing dialog box from a new thread. It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.  </span></span><br/> |
|<span data-ttu-id="6fead-213">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="6fead-214">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-214">**Parameters**</span></span> <br/> | <span data-ttu-id="6fead-215">_piCallback_&ndash;ダイアログボックスが閉じられた後にインスタンス化される**iquickfilingdialogcallback**インターフェイスへの参照。</span><span class="sxs-lookup"><span data-stu-id="6fead-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="6fead-216">新しいスレッドからクイック ファイリング ダイアログ ボックスを表示、 **Run**メソッドを次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="6fead-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

<span data-ttu-id="6fead-217">**TreeCollapsedState**</span><span class="sxs-lookup"><span data-stu-id="6fead-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-218">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-218">**Description**</span></span> <br/> |<span data-ttu-id="6fead-219">階層ツリーを展開または縮小する必要があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6fead-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="6fead-220">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="6fead-221">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-221">**Parameters**</span></span> <br/> | <span data-ttu-id="6fead-222">_tcs_では、ツリーを展開するか、折りたたまれているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6fead-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="6fead-223">**NotebookFilterOut**</span><span class="sxs-lookup"><span data-stu-id="6fead-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-224">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-224">**Description**</span></span> <br/> |<span data-ttu-id="6fead-225">ノート パソコンの種類別に表示の一覧をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="6fead-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="6fead-226">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="6fead-227">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-227">**Parameters**</span></span> <br/> | <span data-ttu-id="6fead-228">_nfo_ - は、ボックスの一覧からフィルターを適用するのには、ノートブックのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="6fead-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="6fead-229">**ShowCreateNewNotebook**</span><span class="sxs-lookup"><span data-stu-id="6fead-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-230">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-230">**Description**</span></span> <br/> |<span data-ttu-id="6fead-231">新規のノートブックの作成] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="6fead-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="6fead-232">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="6fead-233">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-233">**Parameters**</span></span> <br/> |<span data-ttu-id="6fead-234">なし</span><span class="sxs-lookup"><span data-stu-id="6fead-234">None</span></span>  <br/> |
   
<span data-ttu-id="6fead-235">**addinitialeditor**</span><span class="sxs-lookup"><span data-stu-id="6fead-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-236">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-236">**Description**</span></span> <br/> |<span data-ttu-id="6fead-237">クイック ファイリング] ダイアログ ボックスで、ノートを初期のエディターとしてユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="6fead-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="6fead-238">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="6fead-239">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-239">**Parameters**</span></span> <br/> | <span data-ttu-id="6fead-p124">_initialEditor_のノートブックには、エディターとして追加するユーザーの電子メール アドレス。クイック ファイリング] ダイアログ ボックスを使用してノートブックを作成するときに初期のすべてのエディターで自動的に共有されます。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p124">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook. When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.  </span></span><br/> |
   
<span data-ttu-id="6fead-242">**clearinitialeditors**</span><span class="sxs-lookup"><span data-stu-id="6fead-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-243">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-243">**Description**</span></span> <br/> |<span data-ttu-id="6fead-244">クイック ファイリング ダイアログ ボックスからすべての最初のエディターを削除します。</span><span class="sxs-lookup"><span data-stu-id="6fead-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="6fead-245">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="6fead-246">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-246">**Parameters**</span></span> <br/> |<span data-ttu-id="6fead-247">なし</span><span class="sxs-lookup"><span data-stu-id="6fead-247">None</span></span>  <br/> |
   
<span data-ttu-id="6fead-248">**showsharinghyperlink**</span><span class="sxs-lookup"><span data-stu-id="6fead-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-249">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-249">**Description**</span></span> <br/> |<span data-ttu-id="6fead-250">クイック ファイリング] ダイアログ ボックスで、共有のヘルプ ハイパーリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6fead-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="6fead-251">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="6fead-252">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-252">**Parameters**</span></span> <br/> |<span data-ttu-id="6fead-253">なし</span><span class="sxs-lookup"><span data-stu-id="6fead-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="6fead-254">iquickfilingdialogcallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6fead-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="6fead-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="6fead-255"></span></span>

<span data-ttu-id="6fead-p125">このインターフェイス、ダイアログ ボックスを閉じた後、ダイアログ ボックスのプロパティにアクセスすることができます。OneNote 2013は、ダイアログ ボックスを閉じると、このインターフェイスの **IQuickFilingDialogCallback.OnDialogClose**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6fead-p125">This interface allows the user to access the dialog box properties after the dialog box closes. Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="6fead-258">このインターフェイスを継承するクラスを定義するのには。</span><span class="sxs-lookup"><span data-stu-id="6fead-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="6fead-259">メソッド</span><span class="sxs-lookup"><span data-stu-id="6fead-259">Methods</span></span>

<span data-ttu-id="6fead-260">次のセクションは以前詳細なインターフェイスに関連付けられたメソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6fead-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="6fead-261">**ondialogclosed**</span><span class="sxs-lookup"><span data-stu-id="6fead-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fead-262">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fead-262">**Description**</span></span> <br/> |<span data-ttu-id="6fead-p126">キャプチャ] ダイアログ ボックスで、ユーザーの選択を使用して機能を追加することができます。クイック ファイリング] ダイアログ ボックスを閉じた後に、このメソッドは呼び出されます。このメソッドは、 **IQuickFilingDialogCallback**インタ フェースを定義する必要がある関数です。 </span><span class="sxs-lookup"><span data-stu-id="6fead-p126">Enables users to add functionality to capture and use the user selection from the dialog box. This method is called after the Quick Filing dialog box is closed. This method is a function that **IQuickFilingDialogCallback** interfaces have to define.  </span></span><br/> |
|<span data-ttu-id="6fead-266">**構文**</span><span class="sxs-lookup"><span data-stu-id="6fead-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="6fead-267">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6fead-267">**Parameters**</span></span> <br/> | <span data-ttu-id="6fead-268">_ダイアログ_&ndash; **ondialogclose**メソッドを呼び出した**iquickfilingdialog**オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6fead-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="6fead-p127">次の使用例は、サンプルの **IQuickFilingDialogCallback**インターフェイスです。 **OnDialogClose**メソッドは、ユーザーの選択クイック ファイリング] ダイアログ ボックスでコンソールに出力します。</span><span class="sxs-lookup"><span data-stu-id="6fead-p127">The following example is a sample **IQuickFilingDialogCallback** interface. The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a><span data-ttu-id="6fead-271">例</span><span class="sxs-lookup"><span data-stu-id="6fead-271">Example</span></span>
<span data-ttu-id="6fead-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="6fead-272"></span></span>

<span data-ttu-id="6fead-p128">次のコード例では、カスタマイズされたタイトル、説明、最近の結果のリスト、ツリーの深さ、] チェック ボックスおよびボタンは、クイック ファイリング ダイアログ ボックスを開きます。ユーザーのボタンを押して、項目を選択して、ダイアログ ボックスを閉じると、コンソール ウィンドウでチェック ボックスの状態が表示されます。有効になっているページのボタンを表示するには、ユーザーはツリーの深さはのセクションに設定されているため、ページを検索し、選択する必要があります。ダイアログ ボックスは任意のウィンドウの子ウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="6fead-p128">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons. The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed. To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections. The dialog box is not a child of any window.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="6fead-277">関連項目</span><span class="sxs-lookup"><span data-stu-id="6fead-277">See also</span></span>

- [<span data-ttu-id="6fead-278">OneNote の開発者用リファレンス</span><span class="sxs-lookup"><span data-stu-id="6fead-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

