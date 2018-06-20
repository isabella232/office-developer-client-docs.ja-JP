---
title: PidTagFormHostMap の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9e0316ead2adf00619bd87c57946ba72ed01f4b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802793"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="e67e9-103">PidTagFormHostMap の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e67e9-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="e67e9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e67e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e67e9-105">使用可能なフォームのホストのマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e67e9-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e67e9-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e67e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e67e9-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="e67e9-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="e67e9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e67e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e67e9-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="e67e9-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="e67e9-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e67e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="e67e9-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="e67e9-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="e67e9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e67e9-112">Area:</span></span>  <br/> |<span data-ttu-id="e67e9-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="e67e9-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e67e9-114">備考</span><span class="sxs-lookup"><span data-stu-id="e67e9-114">Remarks</span></span>

<span data-ttu-id="e67e9-115">**IMAPIFormProp**インターフェイスの基本構造を変更する場合、クライアント アプリケーションはこのプロパティをプロパティにするには、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と共にを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e67e9-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e67e9-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e67e9-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e67e9-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e67e9-117">Header files</span></span>

<span data-ttu-id="e67e9-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e67e9-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e67e9-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e67e9-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e67e9-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e67e9-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e67e9-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e67e9-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e67e9-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e67e9-122">See also</span></span>



[<span data-ttu-id="e67e9-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e67e9-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e67e9-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e67e9-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e67e9-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e67e9-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e67e9-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e67e9-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

