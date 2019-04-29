---
title: プロパティシートの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430050"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="fda6e-103">プロパティシートの実装</span><span class="sxs-lookup"><span data-stu-id="fda6e-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="fda6e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fda6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fda6e-105">プロパティシートは、オブジェクトのプロパティを表示するダイアログボックスです。</span><span class="sxs-lookup"><span data-stu-id="fda6e-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="fda6e-106">プロパティは読み取り専用であり、ユーザーに対してのみ表示、または読み取り/書き込みが可能であり、ユーザーが変更できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fda6e-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="fda6e-107">プロパティシートには、ページと呼ばれる1つまたは複数の重なった子ウィンドウが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fda6e-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="fda6e-108">各ページには、関連するプロパティのグループを設定するためのコントロールウィンドウが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fda6e-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="fda6e-109">ユーザーがページ間を移動すると、対応するページがプロパティシートの前景になるタブが選択されます。</span><span class="sxs-lookup"><span data-stu-id="fda6e-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="fda6e-110">サービスプロバイダーは、メッセージサービスの構成に関連する最小限のプロパティセットを表示するプロパティシートを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda6e-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="fda6e-111">これらのメッセージサービスのプロパティを変更できるようにする場合は、コントロールパネルなどのクライアントアプリケーションのユーザーに、変更を加えたり、プログラムによって変更を実装したりできるようにします。</span><span class="sxs-lookup"><span data-stu-id="fda6e-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="fda6e-112">プロパティシートを実装して、他の種類のプロパティを表示および編集することはオプションです。</span><span class="sxs-lookup"><span data-stu-id="fda6e-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="fda6e-113">通常、次の状況では、プロパティシートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda6e-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="fda6e-114">クライアントが status オブジェクトの[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドを呼び出す場合。</span><span class="sxs-lookup"><span data-stu-id="fda6e-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="fda6e-115">MAPI がプロバイダーオブジェクトのログオン方法を呼び出したとき。</span><span class="sxs-lookup"><span data-stu-id="fda6e-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="fda6e-116">MAPI がプロバイダーのメッセージサービスのエントリポイント関数を呼び出すとき。</span><span class="sxs-lookup"><span data-stu-id="fda6e-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="fda6e-117">また、トランスポートプロバイダーは、メッセージオプションに関連するプロパティを表示するためのプロパティシートを実装し、アドレス帳プロバイダーは、メッセージングユーザーおよび配布リストに関する詳細情報を表示および編集するためのプロパティシートを実装します。高度な検索新しいユーザーを入力するための基準とテンプレート。</span><span class="sxs-lookup"><span data-stu-id="fda6e-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="fda6e-118">プロパティシートを作成するには、次の3つの方法のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fda6e-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="fda6e-119">ダイアログボックスの場合と同様に、手動で設定します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="fda6e-120">Windows SDK で提供されるプロパティシートコモンコントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="fda6e-121">MAPI 表示テーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="fda6e-122">プロバイダーは最後のオプションを選択する必要があります (表示テーブルを使用してプロパティシートを作成します)。</span><span class="sxs-lookup"><span data-stu-id="fda6e-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="fda6e-123">これは、Windows ユーザーインターフェイスを操作する必要がなくなるため、最も簡単なオプションです。</span><span class="sxs-lookup"><span data-stu-id="fda6e-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="fda6e-124">メッセージサービスのプロパティの表示テーブルから構築されたプロパティシートを実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="fda6e-125">現在のプロファイルのセクションを開くには、 [imapisupport:: openprofile](imapisupport-openprofilesection.md)セクションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="fda6e-126">[MAPIUID](mapiuid.md)または NULL を渡して、プロバイダーのプロファイルセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="fda6e-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="fda6e-127">プロパティデータオブジェクトを作成するには、 [createiprop](createiprop.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="fda6e-128">プロファイルセクションの[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを呼び出して、すべてのセクションのプロパティをプロパティデータオブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="fda6e-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="fda6e-129">表示テーブルを作成するには、プロパティシートに表示されるコントロールを記述し、 [builddisplaytable](builddisplaytable.md)関数を呼び出すか、またはカスタムコードを実装して、1つまたは複数の[dtpage](dtpage.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="fda6e-130">呼び出し[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)は、コピーされたプロパティを持つプロパティシートを表示します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="fda6e-131">_lpconfigdata_パラメーターとしてプロパティデータオブジェクトへのポインターを渡し、 _lpconfigdata_パラメーターとして表示テーブルへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="fda6e-132">このプロパティシートの既定のアクセスモードを無効にする場合は、読み取り専用プロパティを表す表示テーブル内の各コントロールに対して DT_EDITABLE フラグを設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="fda6e-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="fda6e-133">プロパティシートですべての変更を行ったら、プロパティデータオブジェクトの**imapiprop:: CopyTo**メソッドを呼び出して、変更したプロパティをプロファイルセクションにコピーします。</span><span class="sxs-lookup"><span data-stu-id="fda6e-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="fda6e-134">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fda6e-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="fda6e-135">表示テーブルの詳細については、「[表の実装](display-table-implementation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fda6e-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="fda6e-136">コントロールの実装については、「[コントロールオブジェクトの実装](control-object-implementation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fda6e-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="fda6e-137">ユーザーが表示テーブルリストボックスで選択したコントロールのインデックスを取得するには、ユーザーが **[OK]** または [**適用**] をクリックするまで待機します。</span><span class="sxs-lookup"><span data-stu-id="fda6e-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="fda6e-138">この時点で、選択されているアイテムのエントリ id は、 [dtbllbx](dtbllbx.md)構造体の**ulprsetproperty**メンバーによって指定されたプロパティの値として、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスに書き戻されます。</span><span class="sxs-lookup"><span data-stu-id="fda6e-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="fda6e-139">リストボックスのアイテムを追加または削除できるようにする必要がある場合は、表示テーブルと[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="fda6e-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="fda6e-140">代わりに、comdlg32 ファイルに含まれている Win32 プロパティシート API を使用して、プロパティシートを実装することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="fda6e-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fda6e-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="fda6e-141">See also</span></span>



[<span data-ttu-id="fda6e-142">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="fda6e-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

