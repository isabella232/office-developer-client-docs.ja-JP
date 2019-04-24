---
title: 既定のメッセージ ストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348602"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="10910-103">既定のメッセージ ストアを開く</span><span class="sxs-lookup"><span data-stu-id="10910-103">Opening the default message store</span></span>

<span data-ttu-id="10910-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10910-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10910-105">特定のセッションでは、1つのメッセージストアが既定のメッセージストアとして機能します。</span><span class="sxs-lookup"><span data-stu-id="10910-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="10910-106">既定のメッセージストアには、次のような特性があります。</span><span class="sxs-lookup"><span data-stu-id="10910-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="10910-107">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティは TRUE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="10910-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="10910-108">STATUS_DEFAULT_STORE フラグは、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティで設定されます。</span><span class="sxs-lookup"><span data-stu-id="10910-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="10910-109">MAPI は、メッセージストアが開かれたときに、検索結果、共通ビュー、個人用ビューの IPM サブツリーとルートフォルダーを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="10910-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="10910-110">これらのフォルダーの詳細については、「 [IPM Subtree](ipm-subtree.md) and [MAPI Special folders](mapi-special-folders.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="10910-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="10910-111">既定のメッセージストアのエントリ識別子を取得するには、 [imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)を呼び出して、メッセージストアテーブルを開き、 [hrqueryallrows](hrqueryallrows.md)への呼び出しに適切な制限を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10910-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="10910-112">**hrqueryallrows**は、既定のメッセージストアを表す1行の行セットを返します。</span><span class="sxs-lookup"><span data-stu-id="10910-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="10910-113">**hrqueryallrows**に渡す制限は、次のいずれかの形式で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="10910-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="10910-114">**SAndRestriction**構造体を使用して結合する**と**、次のような制限があります。</span><span class="sxs-lookup"><span data-stu-id="10910-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="10910-115">**PR_DEFAULT_STORE**プロパティが存在するかどうかをテストするために、 **sexistrestriction**構造を使用する存在する制限。</span><span class="sxs-lookup"><span data-stu-id="10910-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="10910-116">**PR_DEFAULT_STORE**プロパティの TRUE 値をチェックするために[spropertyrestriction](spropertyrestriction.md)構造を使用するプロパティ制限。</span><span class="sxs-lookup"><span data-stu-id="10910-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="10910-117">**PR_RESOURCE_FLAGS**プロパティに対するマスクとして STATUS_DEFAULT_STORE を適用するために[sbitmaskrestriction](sbitmaskrestriction.md)構造を使用するビットマスク制限。</span><span class="sxs-lookup"><span data-stu-id="10910-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="10910-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="10910-118">See also</span></span>

- [<span data-ttu-id="10910-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="10910-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="10910-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="10910-120">SAndRestriction</span></span>](sandrestriction.md)

