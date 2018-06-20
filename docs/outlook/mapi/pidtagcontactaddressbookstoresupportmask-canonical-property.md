---
title: PidTagContactAddressBookStoreSupportMask の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5cd113c263c97ba306fcf7bf97c750e710eac922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802579"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a><span data-ttu-id="75151-103">PidTagContactAddressBookStoreSupportMask の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="75151-103">PidTagContactAddressBookStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="75151-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75151-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75151-105">連絡先フォルダーを含むストアから取得した**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) のプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="75151-105">Contains the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) property obtained from the store that contains the Contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75151-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="75151-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75151-107">PR_CONTAB_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="75151-107">PR_CONTAB_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="75151-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="75151-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75151-109">0x6611</span><span class="sxs-lookup"><span data-stu-id="75151-109">0x6611</span></span>  <br/> |
|<span data-ttu-id="75151-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="75151-110">Data type:</span></span>  <br/> |<span data-ttu-id="75151-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75151-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75151-112">領域:</span><span class="sxs-lookup"><span data-stu-id="75151-112">Area:</span></span>  <br/> |<span data-ttu-id="75151-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="75151-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75151-114">備考</span><span class="sxs-lookup"><span data-stu-id="75151-114">Remarks</span></span>

<span data-ttu-id="75151-115">連絡先アドレス帳プロバイダーは、このプロパティを使用して、ストアのサポートされている機能の妥当性を評価します。</span><span class="sxs-lookup"><span data-stu-id="75151-115">The Contact Address Book provider uses this property to evaluate the adequacy of the store's supported features.</span></span> <span data-ttu-id="75151-116">これは、連絡先のアドレス帳コンテナー、および連絡先のアドレス帳コンテナーのテーブル内の列のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="75151-116">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75151-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="75151-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="75151-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="75151-118">Header files</span></span>

<span data-ttu-id="75151-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75151-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="75151-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="75151-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="75151-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75151-121">Mapitags.h</span></span>
  
> <span data-ttu-id="75151-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="75151-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75151-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="75151-123">See also</span></span>



[<span data-ttu-id="75151-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="75151-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75151-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="75151-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75151-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="75151-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75151-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="75151-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

