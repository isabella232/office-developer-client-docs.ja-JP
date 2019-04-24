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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ea9938ca9f8dd0b25cf2de5199178a76e17b6d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361181"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a><span data-ttu-id="352ec-103">PidTagTnefUnprocessedProps 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="352ec-103">PidTagTnefUnprocessedProps Canonical Property</span></span>

  
  
<span data-ttu-id="352ec-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="352ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="352ec-105">トランスポートのニュートラルカプセル化形式 (TNEF) をフィルタリングするときにプロパティをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="352ec-105">Serializes properties when filtering Transport Neutral Encapsulation Format (TNEF).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="352ec-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="352ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="352ec-107">PR_TNEF_UNPROCESSED_PROPS</span><span class="sxs-lookup"><span data-stu-id="352ec-107">PR_TNEF_UNPROCESSED_PROPS</span></span>  <br/> |
|<span data-ttu-id="352ec-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="352ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="352ec-109">0x0E9C</span><span class="sxs-lookup"><span data-stu-id="352ec-109">0x0E9C</span></span>  <br/> |
|<span data-ttu-id="352ec-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="352ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="352ec-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="352ec-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="352ec-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="352ec-112">Area:</span></span>  <br/> |<span data-ttu-id="352ec-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="352ec-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="352ec-114">解説</span><span class="sxs-lookup"><span data-stu-id="352ec-114">Remarks</span></span>

<span data-ttu-id="352ec-115">Microsoft outlook および outlook Web Access (OWA) によって、元の tnef を保存するために使用されます。この場合、ストア内に作成できない名前付きプロパティが tnef に含まれています。</span><span class="sxs-lookup"><span data-stu-id="352ec-115">Used by Microsoft Outlook and Outlook Web Access (OWA) for saving the original TNEF in cases where the TNEF contains named properties that cannot be created in the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="352ec-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="352ec-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="352ec-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="352ec-117">Header files</span></span>

<span data-ttu-id="352ec-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="352ec-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="352ec-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="352ec-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="352ec-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="352ec-120">Mapitags.h</span></span>
  
> <span data-ttu-id="352ec-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="352ec-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="352ec-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="352ec-122">See also</span></span>



[<span data-ttu-id="352ec-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="352ec-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="352ec-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="352ec-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="352ec-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="352ec-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="352ec-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="352ec-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

