---
title: 表示テーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3e31dd7b25b3abf333505c8bde57f61be7a10901
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580608"
---
# <a name="display-table-implementation"></a><span data-ttu-id="87fed-103">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="87fed-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="87fed-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87fed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87fed-105">表示テーブルを使用して、プロパティ シートでは、1 つまたは複数のタブ付きプロパティ ページを表示して、おそらく 1 つまたは複数のプロパティを編集するのには専用の特別なダイアログ ボックスで構成されるを表示します。</span><span class="sxs-lookup"><span data-stu-id="87fed-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="87fed-106">関連付けられているテーブルは、すべてのディスプレイで、 [IAttach: IMAPIProp](iattachimapiprop.md)インターフェイスの実装です。</span><span class="sxs-lookup"><span data-stu-id="87fed-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="87fed-107">[IMAPIProp](imapipropiunknown.md)の実装では、プロパティ シートに記載されているプロパティのデータを保持します。</span><span class="sxs-lookup"><span data-stu-id="87fed-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="87fed-108">ディスプレイ テーブル内の行は、プロパティ シートのコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="87fed-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="87fed-109">ほとんどのコントロールは、 **IMAPIProp**の実装と管理プロパティに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="87fed-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="87fed-110">ユーザーは、変更可能なコントロールの値を変更するときは、対応するプロパティが更新されます。</span><span class="sxs-lookup"><span data-stu-id="87fed-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="87fed-111">表示テーブルの各列は、プロパティ シート、種類、関連付けられている構造体、および識別子の位置など、コントロールのプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="87fed-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="87fed-112">必要な表示のテーブルの列の一覧については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87fed-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="87fed-113">MAPI を参照してプロパティ値表示のテーブルに関連付けられている**IMAPIProp**実装とは、表示された表から直接、クライアント アプリケーションのユーザーにプロパティ シートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="87fed-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="87fed-114">ユーザーは、プロパティ シートでは、コントロールで値を変更する MAPI が呼び出され、コントロールの DT_SET_IMMEDIATE フラグが設定されている場合は、変更されたコントロールを保存するのには[IMAPIProp::SetProps](imapiprop-setprops.md)です。</span><span class="sxs-lookup"><span data-stu-id="87fed-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="87fed-115">DT_SET_IMMEDIATE フラグが設定されていないコントロールは、ユーザーが、[ **OK** ] または [**今すぐ適用**] ボタンをクリックしてダイアログ ボックスを閉じるときに、プロパティへの変更は保存されます。</span><span class="sxs-lookup"><span data-stu-id="87fed-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="87fed-116">これらのボタンまたは **[キャンセル**] ボタンのいずれかをクリックすると、MAPI は、ビューからプロパティ シートを削除します。</span><span class="sxs-lookup"><span data-stu-id="87fed-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="87fed-117">**IMAPIProp**実装では、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すと、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを要求するか、継承することで MAPI が、表示テーブルへのアクセスを取得します。[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)など、MAPI に対して行った呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="87fed-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="87fed-118">最初のアクセス方法は、ユーザーまたは配布リストのメッセージに関する詳細を表示するアドレス帳プロバイダーが求められたときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="87fed-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="87fed-119">次の処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="87fed-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="87fed-120">クライアントは、 [IAddrBook::Details](iaddrbook-details.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="87fed-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="87fed-121">MAPI では、選択したエントリを表すメッセージのユーザーにアクセスするためのアドレス帳プロバイダーの[IABLogon::OpenEntry](iablogon-openentry.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="87fed-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="87fed-122">MAPI では、 **PR_DETAILS_TABLE**プロパティで、[詳細情報] ダイアログ ボックスに表示された表を取得するために、メッセージング ユーザーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="87fed-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="87fed-123">MAPI では、情報を含むユーザーの相互作用を処理します] ダイアログ ボックスを表示し、ユーザーが終了したときに削除します。</span><span class="sxs-lookup"><span data-stu-id="87fed-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="87fed-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="87fed-124">See also</span></span>



[<span data-ttu-id="87fed-125">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="87fed-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

