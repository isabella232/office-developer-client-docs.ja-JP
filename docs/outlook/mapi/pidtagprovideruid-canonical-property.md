---
title: PidTagProviderUid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cca22b466b1e0d2da9ca9cc009586df08316270c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581056"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="2afbc-103">PidTagProviderUid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2afbc-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="2afbc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2afbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2afbc-105">メッセージを処理するサービス プロバイダーの**MAPIUID**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2afbc-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2afbc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2afbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2afbc-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="2afbc-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="2afbc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2afbc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2afbc-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="2afbc-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="2afbc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2afbc-110">Data type:</span></span>  <br/> |<span data-ttu-id="2afbc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2afbc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2afbc-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2afbc-112">Area:</span></span>  <br/> |<span data-ttu-id="2afbc-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="2afbc-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2afbc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2afbc-114">Remarks</span></span>

<span data-ttu-id="2afbc-115">このプロパティは、すべてのサービス プロバイダーによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="2afbc-115">This property is computed by all service providers.</span></span> <span data-ttu-id="2afbc-116">[MAPIUID](mapiuid.md)構造体には、関連付けられている、通常、ハードコーディングによって、プロバイダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2afbc-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="2afbc-117">通常は、特定のプロバイダーから提供されているアドレス帳コンテナーのみに興味を持っているクライアント アプリケーションによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="2afbc-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="2afbc-118">このプロパティは、プロバイダーのテーブルの列のエントリとしてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="2afbc-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2afbc-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2afbc-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2afbc-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2afbc-120">Header files</span></span>

<span data-ttu-id="2afbc-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2afbc-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="2afbc-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2afbc-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="2afbc-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2afbc-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2afbc-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2afbc-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2afbc-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="2afbc-125">See also</span></span>



[<span data-ttu-id="2afbc-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2afbc-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2afbc-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2afbc-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2afbc-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2afbc-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2afbc-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2afbc-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

