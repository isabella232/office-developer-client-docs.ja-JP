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
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="70b18-103">PidTagOwnStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="70b18-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="70b18-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70b18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70b18-105">トランスポートの緊密に結合されたメッセージ ストアのエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="70b18-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70b18-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="70b18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70b18-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="70b18-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="70b18-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="70b18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70b18-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="70b18-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="70b18-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="70b18-110">Data type:</span></span>  <br/> |<span data-ttu-id="70b18-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="70b18-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="70b18-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="70b18-112">Area:</span></span>  <br/> |<span data-ttu-id="70b18-113">メッセージ ストアのプロパティ</span><span class="sxs-lookup"><span data-stu-id="70b18-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70b18-114">注釈</span><span class="sxs-lookup"><span data-stu-id="70b18-114">Remarks</span></span>

<span data-ttu-id="70b18-115">このプロパティは、緊密に結合されたストアのエントリ識別子 (存在する場合) を指定します。</span><span class="sxs-lookup"><span data-stu-id="70b18-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="70b18-116">たとえば、MAPI スプーラーがトランスポート プロバイダーをストアに接続できるよう、トランスポート プロバイダーはプライベート フォルダー ストアエントリ識別子を指定できます。</span><span class="sxs-lookup"><span data-stu-id="70b18-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="70b18-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="70b18-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="70b18-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="70b18-118">Header files</span></span>

<span data-ttu-id="70b18-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70b18-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="70b18-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="70b18-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="70b18-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="70b18-121">Mapitags.h</span></span>
  
> <span data-ttu-id="70b18-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="70b18-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70b18-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="70b18-123">See also</span></span>



[<span data-ttu-id="70b18-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="70b18-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70b18-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="70b18-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70b18-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="70b18-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70b18-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="70b18-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

