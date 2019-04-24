---
title: 表示テーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339950"
---
# <a name="display-table-implementation"></a><span data-ttu-id="4ee2b-103">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="4ee2b-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="4ee2b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ee2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ee2b-105">表示テーブルは、プロパティシートを表示するために使用されます。このダイアログボックスには、1つまたは複数のプロパティを表示して編集するための専用のタブ付きプロパティページから構成されます。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="4ee2b-106">すべての表示テーブルに関連付けられているのは、 [iattach: imapiprop](iattachimapiprop.md)インターフェイスの実装です。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="4ee2b-107">[imapiprop](imapipropiunknown.md)の実装は、プロパティシートに表示されるプロパティデータを保持します。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="4ee2b-108">表示テーブル内の行は、プロパティシートのコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="4ee2b-109">ほとんどのコントロールは、 **imapiprop**の実装で管理されるプロパティに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="4ee2b-110">ユーザーが変更可能なコントロールの値を変更すると、対応するプロパティが更新されます。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="4ee2b-111">表示テーブル内の列は、コントロールのプロパティを表します。たとえば、プロパティシート内の位置、種類、関連付けられた構造体、識別子などがあります。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="4ee2b-112">必要な表示テーブル列の完全な一覧については、「[表の表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="4ee2b-113">MAPI では、表示テーブルに関連付けられている**imapiprop**実装のプロパティ値、または直接表示テーブルからプロパティ値を読み取ることによって、クライアントアプリケーションのユーザーにプロパティシートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="4ee2b-114">ユーザーがプロパティシートを使用してコントロールの値を変更すると、MAPI は[imapiprop:: setprops](imapiprop-setprops.md)を呼び出して、コントロールの DT_SET_IMMEDIATE フラグが設定されている場合は、変更されたコントロールを保存します。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="4ee2b-115">DT_SET_IMMEDIATE フラグが設定されていないコントロールでは、ユーザーが **[OK** ] または [**今すぐ適用**] ボタンをクリックしてダイアログボックスを閉じたときに、プロパティの変更が保存されます。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="4ee2b-116">これらのボタンのいずれか、または **[キャンセル**] ボタンがクリックされると、MAPI はプロパティシートをビューから削除します。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="4ee2b-117">MAPI は、 **imapiprop**の実装で[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求するか、またはこのプロパティを継承することによって、表示テーブルへのアクセスを取得します。[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)など、MAPI に対して行った通話。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="4ee2b-118">最初のアクセス方法は、アドレス帳プロバイダーがメッセージングユーザーまたは配布リストに関する詳細を表示するように求められた場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="4ee2b-119">次の処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="4ee2b-120">クライアントが[IAddrBook::D etails](iaddrbook-details.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="4ee2b-121">MAPI は、アドレス帳プロバイダーの[IABLogon:: openentry](iablogon-openentry.md)メソッドを呼び出して、選択されたエントリを表すメッセージングユーザーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="4ee2b-122">MAPI は、メッセージングユーザーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_DETAILS_TABLE**プロパティ、[詳細] ダイアログボックスの表示テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="4ee2b-123">MAPI はダイアログボックスを表示し、ユーザーの情報の操作を処理して、ユーザーが終了したときに削除します。</span><span class="sxs-lookup"><span data-stu-id="4ee2b-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4ee2b-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ee2b-124">See also</span></span>



[<span data-ttu-id="4ee2b-125">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="4ee2b-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

