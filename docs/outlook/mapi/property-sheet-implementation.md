---
title: プロパティ シートの実装
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
# <a name="property-sheet-implementation"></a><span data-ttu-id="919df-103">プロパティ シートの実装</span><span class="sxs-lookup"><span data-stu-id="919df-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="919df-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="919df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="919df-105">プロパティ シートは、オブジェクトのプロパティを表示するためのダイアログ ボックスです。</span><span class="sxs-lookup"><span data-stu-id="919df-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="919df-106">プロパティは読み取り専用で、ユーザーがそれらを表示するか、読み取り/書き込みのみを有効にし、ユーザーが変更を加えるのを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="919df-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="919df-107">プロパティ シートには、ページと呼ばれる 1 つ以上の重なり合う子ウィンドウが含まれます。</span><span class="sxs-lookup"><span data-stu-id="919df-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="919df-108">各ページには、関連するプロパティのグループを設定するコントロール ウィンドウが含まれる。</span><span class="sxs-lookup"><span data-stu-id="919df-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="919df-109">ユーザーは、対応するページをプロパティ シートの前景に移動するタブを選択して、ページ間を移動します。</span><span class="sxs-lookup"><span data-stu-id="919df-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="919df-110">サービス プロバイダーは、メッセージ サービスの構成に関連する最小限のプロパティ セットを表示するプロパティ シートを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="919df-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="919df-111">これらのメッセージ サービスのプロパティを変更できる場合は、コントロール パネルなどのクライアント アプリケーションのユーザーが変更を加えるか、プログラムによって変更を実装できます。</span><span class="sxs-lookup"><span data-stu-id="919df-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="919df-112">他の種類のプロパティを表示および編集するためのプロパティ シートの実装はオプションです。</span><span class="sxs-lookup"><span data-stu-id="919df-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="919df-113">通常、次の状況でプロパティ シートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="919df-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="919df-114">クライアントが状態オブジェクトの [IMAPIStatus::SettingsDialog メソッドを呼び出す](imapistatus-settingsdialog.md) 場合。</span><span class="sxs-lookup"><span data-stu-id="919df-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="919df-115">MAPI がプロバイダー オブジェクトのログオン メソッドを呼び出す場合。</span><span class="sxs-lookup"><span data-stu-id="919df-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="919df-116">MAPI がプロバイダーのメッセージ サービスのエントリ ポイント関数を呼び出す場合。</span><span class="sxs-lookup"><span data-stu-id="919df-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="919df-117">トランスポート プロバイダーは、メッセージ オプションに関連するプロパティを表示するためのプロパティ シートも実装し、アドレス帳プロバイダーは、メッセージング ユーザーと配布リスト、高度な検索条件、および新しいユーザーを入力するためのテンプレートに関する詳細情報を表示および編集するためのプロパティ シートを実装します。</span><span class="sxs-lookup"><span data-stu-id="919df-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="919df-118">次の 3 つの方法のいずれかを使用して、プロパティ シートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="919df-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="919df-119">ダイアログ ボックスと同じ方法で手動で実行します。</span><span class="sxs-lookup"><span data-stu-id="919df-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="919df-120">SDK のプロパティ シート共通コントロールを使用Windowsします。</span><span class="sxs-lookup"><span data-stu-id="919df-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="919df-121">MAPI 表示テーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="919df-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="919df-122">プロバイダーは、最後のオプションを選択する必要があります (表示テーブルを使用してプロパティ シートを作成します)。</span><span class="sxs-lookup"><span data-stu-id="919df-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="919df-123">これは、ユーザー インターフェイスを操作する必要が無いので、最もWindowsです。</span><span class="sxs-lookup"><span data-stu-id="919df-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="919df-124">メッセージ サービスのプロパティの表示テーブルから構築されたプロパティ シートを実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="919df-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="919df-125">[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)を呼び出して、現在のプロファイルでセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="919df-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="919df-126">[MAPIUID または NULL を](mapiuid.md)渡して、プロバイダーのプロファイル セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="919df-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="919df-127">[CreateIProp を呼び](createiprop.md)出してプロパティ データ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="919df-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="919df-128">プロファイル セクションの [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを呼び出して、セクションのすべてのプロパティをプロパティ データ オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="919df-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="919df-129">プロパティ シートに表示するコントロールを記述し[、BuildDisplayTable](builddisplaytable.md)関数を呼び出す 1 つ以上の[DTPAGE](dtpage.md)構造を構築するか、カスタム コードを実装して、表示テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="919df-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="919df-130">[IMAPISupport::D oConfigPropsheet を](imapisupport-doconfigpropsheet.md)呼び出して、コピーされたプロパティを持つプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="919df-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="919df-131">プロパティ データ オブジェクトへのポインターを  _lpConfigData_ パラメーターとして渡し、表示テーブルへのポインターを  _lpDisplayTable パラメーターとして渡_ します。</span><span class="sxs-lookup"><span data-stu-id="919df-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="919df-132">このプロパティ シートの既定のアクセス モードを上書きする場合は、読み取り専用プロパティを表す表示テーブルの各コントロールに DT_EDITABLE フラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="919df-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="919df-133">プロパティ シートですべての変更が行われた場合は、プロパティ データ オブジェクトの **IMAPIProp::CopyTo** メソッドを呼び出して、変更したプロパティをプロファイル セクションにコピーし直します。</span><span class="sxs-lookup"><span data-stu-id="919df-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="919df-134">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="919df-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="919df-135">表示テーブルの詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="919df-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="919df-136">コントロールの実装の詳細については、「コントロール オブジェクトの [実装」を参照してください](control-object-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="919df-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="919df-137">表示テーブルリスト ボックスでユーザーが選択したコントロールのインデックスを取得するには、ユーザーが **[OK]** または [適用] をクリックするまで待 **ちます**。</span><span class="sxs-lookup"><span data-stu-id="919df-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="919df-138">この時点で、選択したアイテムのエントリ識別子は [、DTBLLBX](dtbllbx.md)構造体の **ulPRSetProperty** メンバーによって指定されたプロパティの値として [IMAPIProp : IUnknown](imapipropiunknown.md)インターフェイスに書き戻されます。</span><span class="sxs-lookup"><span data-stu-id="919df-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="919df-139">リスト ボックスからアイテムを追加または削除できる必要がある場合は、表示テーブルを使用し [、IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) メソッドは機能しません。</span><span class="sxs-lookup"><span data-stu-id="919df-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="919df-140">代わりに、Win32 プロパティ シート API を使用してプロパティ シートを実装し、そのファイルに含comdlg32.dllしてください。</span><span class="sxs-lookup"><span data-stu-id="919df-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="919df-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="919df-141">See also</span></span>



[<span data-ttu-id="919df-142">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="919df-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

