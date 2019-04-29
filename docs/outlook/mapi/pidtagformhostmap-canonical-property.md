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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433767"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="66e15-103">PidTagFormHostMap 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66e15-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="66e15-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66e15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66e15-105">使用可能なフォームのホストマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="66e15-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66e15-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="66e15-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66e15-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="66e15-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="66e15-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="66e15-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66e15-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="66e15-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="66e15-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="66e15-110">Data type:</span></span>  <br/> |<span data-ttu-id="66e15-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="66e15-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="66e15-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="66e15-112">Area:</span></span>  <br/> |<span data-ttu-id="66e15-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="66e15-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66e15-114">注釈</span><span class="sxs-lookup"><span data-stu-id="66e15-114">Remarks</span></span>

<span data-ttu-id="66e15-115">クライアントアプリケーションは、 **imapiformprop**インターフェイスの基になる構造を変更するときに、このプロパティを**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと共に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66e15-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="66e15-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="66e15-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="66e15-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="66e15-117">Header files</span></span>

<span data-ttu-id="66e15-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66e15-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="66e15-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="66e15-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="66e15-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="66e15-120">Mapitags.h</span></span>
  
> <span data-ttu-id="66e15-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="66e15-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66e15-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="66e15-122">See also</span></span>



[<span data-ttu-id="66e15-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="66e15-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66e15-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66e15-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66e15-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="66e15-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66e15-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="66e15-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

