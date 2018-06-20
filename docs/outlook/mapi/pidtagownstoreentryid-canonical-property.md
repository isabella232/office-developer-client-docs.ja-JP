---
title: PidTagOwnStoreEntryId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b9ea8af971f9a731aecab0ee6f4b8ea67b651643
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803152"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="9da9d-103">PidTagOwnStoreEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9da9d-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9da9d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9da9d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9da9d-105">トランスポートの密結合のメッセージ ストアのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9da9d-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9da9d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9da9d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9da9d-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9da9d-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="9da9d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9da9d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9da9d-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="9da9d-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="9da9d-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9da9d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9da9d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9da9d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9da9d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9da9d-112">Area:</span></span>  <br/> |<span data-ttu-id="9da9d-113">メッセージ ストアのプロパティ</span><span class="sxs-lookup"><span data-stu-id="9da9d-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9da9d-114">備考</span><span class="sxs-lookup"><span data-stu-id="9da9d-114">Remarks</span></span>

<span data-ttu-id="9da9d-115">このプロパティは、いずれかが存在する場合に、密結合のストアのエントリの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="9da9d-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="9da9d-116">たとえば、トランスポート プロバイダーは、個人用のフォルダーは MAPI スプーラーがストアに、トランスポート プロバイダーを接続できるようにするエントリの識別子を格納を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9da9d-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9da9d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9da9d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9da9d-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9da9d-118">Header files</span></span>

<span data-ttu-id="9da9d-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9da9d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9da9d-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9da9d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9da9d-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9da9d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9da9d-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9da9d-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9da9d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9da9d-123">See also</span></span>



[<span data-ttu-id="9da9d-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9da9d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9da9d-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9da9d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9da9d-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9da9d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9da9d-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9da9d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

