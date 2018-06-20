---
title: 既定のメッセージ ストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1eb4e150be68ea01060c7afaed489c8759b576db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801671"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="2a160-103">既定のメッセージ ストアを開く</span><span class="sxs-lookup"><span data-stu-id="2a160-103">Opening the default message store</span></span>

<span data-ttu-id="2a160-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a160-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a160-105">特定のセッションでは、1 つのメッセージ ・ ストアは、既定のメッセージ ストアとして機能します。</span><span class="sxs-lookup"><span data-stu-id="2a160-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="2a160-106">既定のメッセージ ストアには、次の特徴があります。</span><span class="sxs-lookup"><span data-stu-id="2a160-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="2a160-107">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) のプロパティは、TRUE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2a160-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="2a160-108">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティで、STATUS_DEFAULT_STORE フラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="2a160-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="2a160-109">メッセージ ストアを開いたときに、IPM サブツリーおよび検索の結果、一般的なビューと個人用ビューのルート フォルダー MAPI 自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="2a160-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="2a160-110">これらのフォルダーの詳細については、 [IPM サブツリー](ipm-subtree.md)および[MAPI の特別なフォルダー](mapi-special-folders.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a160-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="2a160-111">既定のメッセージ ストアのエントリ id を取得するには、メッセージ ストアのテーブルを開き、 [HrQueryAllRows](hrqueryallrows.md)への呼び出しで適切な制限を適用する[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a160-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="2a160-112">**HrQueryAllRows**には、既定のメッセージ ストアを表す 1 つの行セットの行が返されます。</span><span class="sxs-lookup"><span data-stu-id="2a160-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="2a160-113">**HrQueryAllRows**に渡された制限は、形式は次のいずれかで実行できます。</span><span class="sxs-lookup"><span data-stu-id="2a160-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="2a160-114">結合する**SAndRestriction**構造体を使用して**** 制限します。</span><span class="sxs-lookup"><span data-stu-id="2a160-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="2a160-115">**PR_DEFAULT_STORE**プロパティの存在をテストするのには**SExistRestriction**構造体を使用する制限が存在します。</span><span class="sxs-lookup"><span data-stu-id="2a160-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="2a160-116">**PR_DEFAULT_STORE**プロパティに TRUE の値をチェックする[SPropertyRestriction](spropertyrestriction.md)構造体を使用するプロパティの制限。</span><span class="sxs-lookup"><span data-stu-id="2a160-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="2a160-117">**PR_RESOURCE_FLAGS**プロパティをマスクとして STATUS_DEFAULT_STORE を適用するための[SBitMaskRestriction](sbitmaskrestriction.md)構造体を使用するビットマスクの制限。</span><span class="sxs-lookup"><span data-stu-id="2a160-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2a160-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a160-118">See also</span></span>

- [<span data-ttu-id="2a160-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="2a160-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="2a160-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="2a160-120">SAndRestriction</span></span>](sandrestriction.md)

