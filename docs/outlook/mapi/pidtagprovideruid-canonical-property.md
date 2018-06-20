---
title: PidTagProviderUid の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803212"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="b0f02-103">PidTagProviderUid の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b0f02-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="b0f02-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0f02-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0f02-105">メッセージを処理するサービス プロバイダーの**MAPIUID**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0f02-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0f02-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b0f02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0f02-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="b0f02-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="b0f02-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b0f02-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0f02-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="b0f02-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="b0f02-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b0f02-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0f02-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b0f02-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b0f02-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b0f02-112">Area:</span></span>  <br/> |<span data-ttu-id="b0f02-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="b0f02-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0f02-114">備考</span><span class="sxs-lookup"><span data-stu-id="b0f02-114">Remarks</span></span>

<span data-ttu-id="b0f02-115">このプロパティは、すべてのサービス プロバイダーによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="b0f02-115">This property is computed by all service providers.</span></span> <span data-ttu-id="b0f02-116">[MAPIUID](mapiuid.md)構造体には、関連付けられている、通常、ハードコーディングによって、プロバイダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0f02-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="b0f02-117">通常は、特定のプロバイダーから提供されているアドレス帳コンテナーのみに興味を持っているクライアント アプリケーションによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0f02-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="b0f02-118">このプロパティは、プロバイダーのテーブルの列のエントリとしてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0f02-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b0f02-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b0f02-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b0f02-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b0f02-120">Header files</span></span>

<span data-ttu-id="b0f02-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0f02-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0f02-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b0f02-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0f02-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0f02-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b0f02-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0f02-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0f02-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0f02-125">See also</span></span>



[<span data-ttu-id="b0f02-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b0f02-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0f02-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b0f02-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0f02-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b0f02-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0f02-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b0f02-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

