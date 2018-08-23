---
title: PidTagContactAddressBookStoreSupportMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7219a8936381c498e7b27898f5efae8e40697b59
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565614"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a><span data-ttu-id="4513d-103">PidTagContactAddressBookStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4513d-103">PidTagContactAddressBookStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="4513d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4513d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4513d-105">連絡先フォルダーを含むストアから取得した**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) のプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4513d-105">Contains the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) property obtained from the store that contains the Contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4513d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4513d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4513d-107">PR_CONTAB_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="4513d-107">PR_CONTAB_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="4513d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4513d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4513d-109">0x6611</span><span class="sxs-lookup"><span data-stu-id="4513d-109">0x6611</span></span>  <br/> |
|<span data-ttu-id="4513d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4513d-110">Data type:</span></span>  <br/> |<span data-ttu-id="4513d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4513d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4513d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4513d-112">Area:</span></span>  <br/> |<span data-ttu-id="4513d-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="4513d-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4513d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4513d-114">Remarks</span></span>

<span data-ttu-id="4513d-115">連絡先アドレス帳プロバイダーは、このプロパティを使用して、ストアのサポートされている機能の妥当性を評価します。</span><span class="sxs-lookup"><span data-stu-id="4513d-115">The Contact Address Book provider uses this property to evaluate the adequacy of the store's supported features.</span></span> <span data-ttu-id="4513d-116">これは、連絡先のアドレス帳コンテナー、および連絡先のアドレス帳コンテナーのテーブル内の列のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="4513d-116">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4513d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4513d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4513d-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4513d-118">Header files</span></span>

<span data-ttu-id="4513d-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4513d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4513d-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4513d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4513d-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4513d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4513d-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4513d-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4513d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="4513d-123">See also</span></span>



[<span data-ttu-id="4513d-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4513d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4513d-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4513d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4513d-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4513d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4513d-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4513d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

