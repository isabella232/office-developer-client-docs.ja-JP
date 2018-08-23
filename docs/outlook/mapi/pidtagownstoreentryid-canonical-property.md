---
title: PidTagOwnStoreEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 54014ab25d268c161465349b4e33c6a1df19f140
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591699"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="05aa9-103">PidTagOwnStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05aa9-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="05aa9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05aa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05aa9-105">トランスポートの密結合のメッセージ ストアのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="05aa9-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05aa9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="05aa9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05aa9-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="05aa9-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="05aa9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="05aa9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05aa9-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="05aa9-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="05aa9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="05aa9-110">Data type:</span></span>  <br/> |<span data-ttu-id="05aa9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="05aa9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="05aa9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="05aa9-112">Area:</span></span>  <br/> |<span data-ttu-id="05aa9-113">メッセージ ストアのプロパティ</span><span class="sxs-lookup"><span data-stu-id="05aa9-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05aa9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="05aa9-114">Remarks</span></span>

<span data-ttu-id="05aa9-115">このプロパティは、いずれかが存在する場合に、密結合のストアのエントリの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="05aa9-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="05aa9-116">たとえば、トランスポート プロバイダーは、個人用のフォルダーは MAPI スプーラーがストアに、トランスポート プロバイダーを接続できるようにするエントリの識別子を格納を指定できます。</span><span class="sxs-lookup"><span data-stu-id="05aa9-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="05aa9-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="05aa9-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="05aa9-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="05aa9-118">Header files</span></span>

<span data-ttu-id="05aa9-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05aa9-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="05aa9-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="05aa9-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="05aa9-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="05aa9-121">Mapitags.h</span></span>
  
> <span data-ttu-id="05aa9-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="05aa9-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05aa9-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="05aa9-123">See also</span></span>



[<span data-ttu-id="05aa9-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="05aa9-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05aa9-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="05aa9-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05aa9-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="05aa9-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05aa9-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="05aa9-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

