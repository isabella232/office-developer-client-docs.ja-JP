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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435265"
---
# <a name="display-table-implementation"></a><span data-ttu-id="cb849-103">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="cb849-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="cb849-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb849-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb849-105">表示テーブルは、1 つ以上のプロパティの表示と編集専用の 1 つ以上のタブ付きプロパティ ページで構成される特別なダイアログ ボックスであるプロパティ シートを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb849-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="cb849-106">すべての表示テーブルに関連付けられている [のは、IAttach : IMAPIProp インターフェイス](iattachimapiprop.md) の実装です。</span><span class="sxs-lookup"><span data-stu-id="cb849-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="cb849-107">[IMAPIProp の実装](imapipropiunknown.md)では、プロパティ シートに表示されるプロパティ データが保持されます。</span><span class="sxs-lookup"><span data-stu-id="cb849-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="cb849-108">表示テーブル内の行は、プロパティ シート内のコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="cb849-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="cb849-109">ほとんどのコントロールは、IMAPIProp 実装で管理されている **プロパティに関連付** けできます。</span><span class="sxs-lookup"><span data-stu-id="cb849-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="cb849-110">ユーザーが変更可能なコントロールの値を変更すると、対応するプロパティが更新されます。</span><span class="sxs-lookup"><span data-stu-id="cb849-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="cb849-111">表示テーブル内の列は、プロパティ シート内の位置、その種類、関連する構造、識別子など、コントロールのプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="cb849-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="cb849-112">必要な表示テーブル列の完全な一覧については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="cb849-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="cb849-113">MAPI は、表示テーブルまたは表示テーブルに関連付けられた **IMAPIProp** 実装のプロパティ値を直接読み取って、クライアント アプリケーションのユーザーにプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="cb849-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="cb849-114">ユーザーがコントロールの値を変更してプロパティ シートを操作すると、MAPI は [IMAPIProp::SetProps](imapiprop-setprops.md) を呼び出して、コントロールの DT_SET_IMMEDIATE フラグが設定されている場合に変更されたコントロールを保存します。</span><span class="sxs-lookup"><span data-stu-id="cb849-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="cb849-115">DT_SET_IMMEDIATE フラグが設定DT_SET_IMMEDIATEコントロールの場合、ユーザーが **[OK]** または [今すぐ適用] ボタンをクリックしてダイアログ ボックスを閉じ、プロパティに対する変更 **が保存** されます。</span><span class="sxs-lookup"><span data-stu-id="cb849-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="cb849-116">これらのボタンまたは [キャンセル]ボタンのいずれかをクリックすると、MAPI はプロパティ シートをビューから削除します。</span><span class="sxs-lookup"><span data-stu-id="cb849-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="cb849-117">MAPI は **、IMAPIProp** 実装で [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出し **、PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求するか [、IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md)などの MAPI に対して行った呼び出しで継承することで、表示テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="cb849-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="cb849-118">最初のアクセス方法は、メッセージング ユーザーまたは配布リストに関する詳細を表示するアドレス帳プロバイダーに求める場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb849-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="cb849-119">次の処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="cb849-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="cb849-120">クライアントは [、IAddrBook::Dメソッドを呼び出](iaddrbook-details.md) します。</span><span class="sxs-lookup"><span data-stu-id="cb849-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="cb849-121">MAPI は、アドレス帳プロバイダーの [IABLogon::OpenEntry](iablogon-openentry.md) メソッドを呼び出して、選択したエントリを表すメッセージング ユーザーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="cb849-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="cb849-122">MAPI は、メッセージング ユーザーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出して **、PR_DETAILS_TABLE** プロパティ 、詳細ダイアログ ボックスの表示テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="cb849-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="cb849-123">MAPI は、ユーザーの情報とのやり取りを処理するダイアログ ボックスを表示し、ユーザーが終了するとそのダイアログ ボックスを削除します。</span><span class="sxs-lookup"><span data-stu-id="cb849-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="cb849-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="cb849-124">See also</span></span>



[<span data-ttu-id="cb849-125">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cb849-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

