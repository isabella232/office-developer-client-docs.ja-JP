---
title: PidTagAbProviderId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802401"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="fbc23-103">PidTagAbProviderId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="fbc23-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="fbc23-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbc23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbc23-105">アドレス帳プロバイダーの[MAPIUID](mapiuid.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fbc23-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbc23-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="fbc23-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fbc23-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="fbc23-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="fbc23-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fbc23-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fbc23-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="fbc23-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="fbc23-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="fbc23-110">Data type:</span></span>  <br/> |<span data-ttu-id="fbc23-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fbc23-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fbc23-112">領域:</span><span class="sxs-lookup"><span data-stu-id="fbc23-112">Area:</span></span>  <br/> |<span data-ttu-id="fbc23-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="fbc23-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbc23-114">備考</span><span class="sxs-lookup"><span data-stu-id="fbc23-114">Remarks</span></span>

<span data-ttu-id="fbc23-115">**MAPIUID**構造体は、このコンテナーの階層内の特定のコンテナーを提供するアドレス帳プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="fbc23-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="fbc23-116">値は、各プロバイダーに固有です。</span><span class="sxs-lookup"><span data-stu-id="fbc23-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="fbc23-117">アドレス帳プロバイダーは、複数の識別子を提供できます。</span><span class="sxs-lookup"><span data-stu-id="fbc23-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="fbc23-118">などの異なる 2 つのコンテナーを提供するプロバイダーは、各コンテナーの一意の識別子を**PR_AB_PROVIDER_ID**で発行できます。</span><span class="sxs-lookup"><span data-stu-id="fbc23-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="fbc23-119">**PR_AB_PROVIDER_ID**は、メッセージ ・ ストアの**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) のプロパティに似ています。</span><span class="sxs-lookup"><span data-stu-id="fbc23-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="fbc23-120">クライアント アプリケーションは、アドレス帳の階層テーブルに関連する行を検索するのには**PR_AB_PROVIDER_ID**を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="fbc23-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fbc23-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fbc23-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fbc23-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fbc23-122">Header files</span></span>

<span data-ttu-id="fbc23-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fbc23-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fbc23-124">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fbc23-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="fbc23-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fbc23-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fbc23-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fbc23-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fbc23-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="fbc23-127">See also</span></span>



[<span data-ttu-id="fbc23-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fbc23-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="fbc23-129">PidTagStoreProvider の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="fbc23-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="fbc23-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fbc23-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fbc23-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="fbc23-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fbc23-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="fbc23-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

