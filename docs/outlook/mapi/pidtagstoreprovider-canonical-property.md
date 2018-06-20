---
title: PidTagStoreProvider の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b634f815d2aedecc716227c6525b846db38ca869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803593"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="24ac5-103">PidTagStoreProvider の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="24ac5-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="24ac5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24ac5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24ac5-105">メッセージ ・ ストアの種類を示すプロバイダー定義の[MAPIUID](mapiuid.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="24ac5-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24ac5-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="24ac5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24ac5-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="24ac5-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="24ac5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="24ac5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24ac5-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="24ac5-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="24ac5-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="24ac5-110">Data type:</span></span>  <br/> |<span data-ttu-id="24ac5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="24ac5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="24ac5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="24ac5-112">Area:</span></span>  <br/> |<span data-ttu-id="24ac5-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="24ac5-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24ac5-114">備考</span><span class="sxs-lookup"><span data-stu-id="24ac5-114">Remarks</span></span>

<span data-ttu-id="24ac5-115">[MAPIUID](mapiuid.md)構造体では、メッセージ ・ ストアの種類を識別します。</span><span class="sxs-lookup"><span data-stu-id="24ac5-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="24ac5-116">値は、メッセージ ストアのオブジェクトに、メッセージ ストア プロバイダーによって計算され、各プロバイダーに固有です。</span><span class="sxs-lookup"><span data-stu-id="24ac5-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="24ac5-117">パブリック フォルダーなど、目的の種類のストアを検索するのにはメッセージ ストアのテーブルを参照するために通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="24ac5-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="24ac5-118">このプロパティは、アドレス帳の**PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) のプロパティに似ています。</span><span class="sxs-lookup"><span data-stu-id="24ac5-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="24ac5-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="24ac5-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="24ac5-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="24ac5-120">Header files</span></span>

<span data-ttu-id="24ac5-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24ac5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="24ac5-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="24ac5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="24ac5-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24ac5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="24ac5-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="24ac5-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24ac5-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="24ac5-125">See also</span></span>



[<span data-ttu-id="24ac5-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="24ac5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24ac5-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="24ac5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24ac5-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="24ac5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24ac5-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="24ac5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

