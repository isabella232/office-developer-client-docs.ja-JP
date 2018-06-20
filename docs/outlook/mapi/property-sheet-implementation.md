---
title: プロパティ シートの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 406451adac3cd73286feb787bd6b4d2f356aa283
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803702"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="1623e-103">プロパティ シートの実装</span><span class="sxs-lookup"><span data-stu-id="1623e-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="1623e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1623e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1623e-105">プロパティ シートは、オブジェクトのプロパティを表示するためのダイアログ ボックスです。</span><span class="sxs-lookup"><span data-stu-id="1623e-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="1623e-106">プロパティは、読み取り専用でのみ表示すること、ユーザーの有効化または変更するユーザーを有効にすると、読み取り/書き込み。</span><span class="sxs-lookup"><span data-stu-id="1623e-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="1623e-107">プロパティ シートには、ページと呼ばれる 1 つまたは複数の重複している子ウィンドウが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1623e-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="1623e-108">各ページには、関連するプロパティのグループを設定するためのコントロールのウィンドウが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1623e-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="1623e-109">ユーザーは、プロパティ シートの前景色に対応するページを表示するタブを選択してページを移動します。</span><span class="sxs-lookup"><span data-stu-id="1623e-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="1623e-110">サービス プロバイダーは、メッセージ サービスの構成に関連するプロパティの最小限のセットを表示するプロパティ シートを実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1623e-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="1623e-111">これらメッセージ サービスのプロパティを変更するを許可する場合を許可するかクライアントのユーザー アプリケーションでは、コントロール パネルで、変更またはプログラムを使用して変更を実装します。</span><span class="sxs-lookup"><span data-stu-id="1623e-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="1623e-112">表示および他の種類のプロパティを編集するプロパティ シートの実装は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="1623e-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="1623e-113">通常、次のような状況でプロパティ シートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1623e-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="1623e-114">クライアントは、状態オブジェクトの[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドを呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="1623e-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="1623e-115">MAPI は、プロバイダー オブジェクトのログオン メソッドを呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="1623e-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="1623e-116">MAPI が、プロバイダーのメッセージ サービスのエントリ ポイント関数を呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="1623e-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="1623e-117">トランスポート プロバイダーは、メッセージのオプションに関連するプロパティを表示するプロパティ シートも実装し、アドレス帳プロバイダー実装のプロパティ シートを表示し、ユーザーと配布リスト、詳細検索のメッセージに関する詳細情報を編集するには抽出条件、および新しいユーザーを入力するためのテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="1623e-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="1623e-118">プロパティ シートを作成するのにには、次の 3 つの手法の 1 つを使用します。</span><span class="sxs-lookup"><span data-stu-id="1623e-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="1623e-119">手動で、任意のダイアログ ボックスと同様です。</span><span class="sxs-lookup"><span data-stu-id="1623e-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="1623e-120">Windows SDK で提供されているプロパティ シートの一般的なコントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="1623e-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="1623e-121">MAPI を使用してテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="1623e-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="1623e-122">プロバイダーは、最後のオプションを選択する必要があります (表示のテーブルを使用してプロパティ シートを作成する)。</span><span class="sxs-lookup"><span data-stu-id="1623e-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="1623e-123">これは、Windows のユーザー インターフェイスを使用する必要があるためにの最も簡単なオプションです。</span><span class="sxs-lookup"><span data-stu-id="1623e-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="1623e-124">メッセージ サービスのプロパティの表示のテーブルから作成されたプロパティ シートを実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="1623e-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="1623e-125">現在のプロファイルのセクションを開くには、 [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1623e-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="1623e-126">プロバイダーのプロファイル セクションを開くには、 [MAPIUID](mapiuid.md)または NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="1623e-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="1623e-127">プロパティのデータ オブジェクトを作成するのには[CreateIProp](createiprop.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1623e-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="1623e-128">プロパティのデータ オブジェクトへのすべてのセクションのプロパティをコピーするのには、プロファイルのセクションの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1623e-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="1623e-129">プロパティ シートと、 [BuildDisplayTable](builddisplaytable.md)関数を呼び出すことで表示するコントロールを記述する 1 つまたは複数の[DTPAGE](dtpage.md)構造体を作成することによって、またはカスタム コードを実装することにより、表示された表を作成します。</span><span class="sxs-lookup"><span data-stu-id="1623e-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="1623e-130">コピーしたプロパティを持つプロパティ シートを表示するのには[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1623e-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="1623e-131">_LpConfigData_パラメーターと、テーブルへのポインターの表示、 _lpDisplayTable_パラメーターとプロパティのデータ オブジェクトへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="1623e-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="1623e-132">このプロパティ シートの既定のアクセス モードをオーバーライドする場合、読み取り専用プロパティを表す表示された表の各コントロールの DT_EDITABLE フラグは設定しません。</span><span class="sxs-lookup"><span data-stu-id="1623e-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="1623e-133">すべての変更を行ったとき、プロパティ シートで、変更されたプロパティを [プロファイル] セクションにコピーするのには、プロパティのデータ オブジェクトの**IMAPIProp::CopyTo**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1623e-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="1623e-134">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1623e-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="1623e-135">テーブルの表示の詳細については、[テーブルの表示の実装](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1623e-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="1623e-136">コントロールを実装する方法の詳細については、[コントロール オブジェクトの実装](control-object-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1623e-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="1623e-137">表示のテーブルのリスト ボックスでユーザーが選択するコントロールのインデックスを取得するには、ユーザーが **[ok]** または [**適用**] をクリックするまで待機します。</span><span class="sxs-lookup"><span data-stu-id="1623e-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="1623e-138">この時点で、選択したアイテムのエントリ id に書き込まれる、 [IMAPIProp: IUnknown](imapipropiunknown.md) [DTBLLBX](dtbllbx.md)構造体の**ulPRSetProperty**のメンバーによって指定されたプロパティの値としてのインタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="1623e-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="1623e-139">追加またはリスト ボックスから項目を削除できる場合は、表示のテーブルと、 [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用して動作しません。</span><span class="sxs-lookup"><span data-stu-id="1623e-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="1623e-140">代わりに、comdlg32.dll ファイルに含まれている Win32 のプロパティ シート API を使用してプロパティ シートを実装することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="1623e-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1623e-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="1623e-141">See also</span></span>



[<span data-ttu-id="1623e-142">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1623e-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

