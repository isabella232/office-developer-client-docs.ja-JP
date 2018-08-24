---
title: PidTagFormHostMap 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c024f71279fac5dbb3d771442d9fbfb8a50e0f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578872"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="27731-103">PidTagFormHostMap 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="27731-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="27731-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27731-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27731-105">使用可能なフォームのホストのマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="27731-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27731-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="27731-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27731-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="27731-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="27731-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="27731-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27731-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="27731-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="27731-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="27731-110">Data type:</span></span>  <br/> |<span data-ttu-id="27731-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="27731-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="27731-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="27731-112">Area:</span></span>  <br/> |<span data-ttu-id="27731-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="27731-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27731-114">注釈</span><span class="sxs-lookup"><span data-stu-id="27731-114">Remarks</span></span>

<span data-ttu-id="27731-115">**IMAPIFormProp**インターフェイスの基本構造を変更する場合、クライアント アプリケーションはこのプロパティをプロパティにするには、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と共にを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27731-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="27731-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="27731-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="27731-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="27731-117">Header files</span></span>

<span data-ttu-id="27731-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27731-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="27731-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="27731-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="27731-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27731-120">Mapitags.h</span></span>
  
> <span data-ttu-id="27731-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="27731-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27731-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="27731-122">See also</span></span>



[<span data-ttu-id="27731-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="27731-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27731-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="27731-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27731-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="27731-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27731-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="27731-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

