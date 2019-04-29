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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427375"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="d193b-103">PidTagOwnStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d193b-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d193b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d193b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d193b-105">トランスポートの密結合メッセージストアのエントリ id を格納します。</span><span class="sxs-lookup"><span data-stu-id="d193b-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d193b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d193b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d193b-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d193b-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d193b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d193b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d193b-109">0x3e06</span><span class="sxs-lookup"><span data-stu-id="d193b-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="d193b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d193b-110">Data type:</span></span>  <br/> |<span data-ttu-id="d193b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d193b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d193b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d193b-112">Area:</span></span>  <br/> |<span data-ttu-id="d193b-113">メッセージストアのプロパティ</span><span class="sxs-lookup"><span data-stu-id="d193b-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d193b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d193b-114">Remarks</span></span>

<span data-ttu-id="d193b-115">このプロパティは、密結合ストアがある場合は、そのエントリ識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="d193b-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="d193b-116">たとえば、トランスポートプロバイダーは、パブリックフォルダーストアエントリ識別子を指定して、MAPI スプーラーがトランスポートプロバイダーをストアに接続できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d193b-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d193b-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d193b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d193b-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d193b-118">Header files</span></span>

<span data-ttu-id="d193b-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d193b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="d193b-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d193b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="d193b-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d193b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="d193b-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d193b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d193b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="d193b-123">See also</span></span>



[<span data-ttu-id="d193b-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d193b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d193b-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d193b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d193b-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d193b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d193b-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d193b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

