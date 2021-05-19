---
title: PidTagOriginalSubject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331144"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="2e08f-103">PidTagOriginalSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e08f-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="2e08f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e08f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e08f-105">メッセージに関するレポートで使用する元のメッセージの件名を格納します。</span><span class="sxs-lookup"><span data-stu-id="2e08f-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e08f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2e08f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e08f-107">PR_ORIGINAL_SUBJECT、PR_ORIGINAL_SUBJECT_A、PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="2e08f-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="2e08f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2e08f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e08f-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="2e08f-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="2e08f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2e08f-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e08f-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e08f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2e08f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2e08f-112">Area:</span></span>  <br/> |<span data-ttu-id="2e08f-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="2e08f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e08f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2e08f-114">Remarks</span></span>

<span data-ttu-id="2e08f-115">これらのプロパティは、元のプロパティ ([PidTagSubject](pidtagsubject-canonical-property.md) **)** プロパティPR_SUBJECT同じ値に設定されています。</span><span class="sxs-lookup"><span data-stu-id="2e08f-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="2e08f-116">件名プロパティは、通常、256 文字未満の小さな文字列であり、メッセージ ストア プロバイダーは、オブジェクト リンクおよび埋め込み (OLE) **IStream** インターフェイスをサポートする義務はありません。</span><span class="sxs-lookup"><span data-stu-id="2e08f-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="2e08f-117">クライアントは、必ず最初に **IMAPIProp** インターフェイスを介してアクセスを試行し、IStream にアクセスMAPI_E_NOT_ENOUGH_MEMORY必要があります。  </span><span class="sxs-lookup"><span data-stu-id="2e08f-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e08f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2e08f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e08f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2e08f-119">Protocol specifications</span></span>

<span data-ttu-id="2e08f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e08f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e08f-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="2e08f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e08f-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e08f-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e08f-123">サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="2e08f-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="2e08f-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e08f-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e08f-125">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e08f-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e08f-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2e08f-126">Header files</span></span>

<span data-ttu-id="2e08f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e08f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e08f-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2e08f-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e08f-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e08f-129">Mapitags.h</span></span>
  
> <span data-ttu-id="2e08f-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2e08f-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e08f-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e08f-131">See also</span></span>



[<span data-ttu-id="2e08f-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2e08f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e08f-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e08f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e08f-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2e08f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e08f-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2e08f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

