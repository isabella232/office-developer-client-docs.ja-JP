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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436028"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="3def9-103">既定のメッセージ ストアを開く</span><span class="sxs-lookup"><span data-stu-id="3def9-103">Opening the default message store</span></span>

<span data-ttu-id="3def9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3def9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3def9-105">特定のセッションでは、1 つのメッセージ ストアが既定のメッセージ ストアとして機能します。</span><span class="sxs-lookup"><span data-stu-id="3def9-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="3def9-106">既定のメッセージ ストアには、次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="3def9-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="3def9-107">プロパティ **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティは TRUE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3def9-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="3def9-108">このSTATUS_DEFAULT_STOREフラグは、プロパティ **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) PR_RESOURCE_FLAGSで設定されます。</span><span class="sxs-lookup"><span data-stu-id="3def9-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="3def9-109">MAPI は、メッセージ ストアを開く際に、検索結果、一般的なビュー、個人用ビューの IPM サブツリーとルート フォルダーを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="3def9-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="3def9-110">これらのフォルダーの詳細については [、「IPM Subtree」および「MAPI Special](ipm-subtree.md) [Folders」を参照してください](mapi-special-folders.md)。</span><span class="sxs-lookup"><span data-stu-id="3def9-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="3def9-111">既定のメッセージ ストアのエントリ識別子を取得するには [、IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) を呼び出してメッセージ ストア テーブルを開き [、HrQueryAllRows](hrqueryallrows.md)の呼び出しで適切な制限を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3def9-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="3def9-112">**HrQueryAllRows は** 、既定のメッセージ ストアを表す 1 行の行セットを返します。</span><span class="sxs-lookup"><span data-stu-id="3def9-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="3def9-113">**HrQueryAllRows** に渡す制限は、次のいずれかの形式で実行できます。</span><span class="sxs-lookup"><span data-stu-id="3def9-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="3def9-114">次 **の組** み合わせに **SAndRestriction 構造を使用する** AND 制限。</span><span class="sxs-lookup"><span data-stu-id="3def9-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="3def9-115">**SExistRestriction** 構造体を使用して、プロパティの存在をテストする **PR_DEFAULT_STOREがあります。**</span><span class="sxs-lookup"><span data-stu-id="3def9-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="3def9-116">[SPropertyRestriction](spropertyrestriction.md)構造体を使用して、プロパティの TRUE 値を確認するプロパティ **PR_DEFAULT_STOREします。**</span><span class="sxs-lookup"><span data-stu-id="3def9-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="3def9-117">[SBitMaskRestriction](sbitmaskrestriction.md)構造体を使用して、STATUS_DEFAULT_STORE プロパティに対してマスクとして適用するビットマスク **PR_RESOURCE_FLAGS** 制限。</span><span class="sxs-lookup"><span data-stu-id="3def9-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3def9-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="3def9-118">See also</span></span>

- [<span data-ttu-id="3def9-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="3def9-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="3def9-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="3def9-120">SAndRestriction</span></span>](sandrestriction.md)

