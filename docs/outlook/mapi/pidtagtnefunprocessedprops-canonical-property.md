---
title: PidTagTnefUnprocessedProps 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ea9938ca9f8dd0b25cf2de5199178a76e17b6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431324"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a><span data-ttu-id="44e7a-103">PidTagTnefUnprocessedProps 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44e7a-103">PidTagTnefUnprocessedProps Canonical Property</span></span>

  
  
<span data-ttu-id="44e7a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44e7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44e7a-105">トランスポート ニュートラル カプセル化形式 (TNEF) をフィルター処理するときにプロパティをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="44e7a-105">Serializes properties when filtering Transport Neutral Encapsulation Format (TNEF).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44e7a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="44e7a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44e7a-107">PR_TNEF_UNPROCESSED_PROPS</span><span class="sxs-lookup"><span data-stu-id="44e7a-107">PR_TNEF_UNPROCESSED_PROPS</span></span>  <br/> |
|<span data-ttu-id="44e7a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="44e7a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44e7a-109">0x0E9C</span><span class="sxs-lookup"><span data-stu-id="44e7a-109">0x0E9C</span></span>  <br/> |
|<span data-ttu-id="44e7a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="44e7a-110">Data type:</span></span>  <br/> |<span data-ttu-id="44e7a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="44e7a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="44e7a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="44e7a-112">Area:</span></span>  <br/> |<span data-ttu-id="44e7a-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="44e7a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44e7a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="44e7a-114">Remarks</span></span>

<span data-ttu-id="44e7a-115">ストアで作成できない名前付きプロパティが TNEF に含まれている場合に、元の TNEF を保存するために Microsoft Outlook および Outlook Web Access (OWA) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="44e7a-115">Used by Microsoft Outlook and Outlook Web Access (OWA) for saving the original TNEF in cases where the TNEF contains named properties that cannot be created in the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44e7a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="44e7a-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="44e7a-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="44e7a-117">Header files</span></span>

<span data-ttu-id="44e7a-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44e7a-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="44e7a-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="44e7a-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="44e7a-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44e7a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="44e7a-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="44e7a-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44e7a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="44e7a-122">See also</span></span>



[<span data-ttu-id="44e7a-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="44e7a-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44e7a-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44e7a-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44e7a-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="44e7a-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44e7a-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="44e7a-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

