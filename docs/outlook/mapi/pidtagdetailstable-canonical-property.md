---
title: PidTagDetailsTable の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802678"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="43b6d-103">PidTagDetailsTable の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="43b6d-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="43b6d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43b6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43b6d-105">埋め込み表示テーブル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="43b6d-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43b6d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="43b6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43b6d-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="43b6d-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="43b6d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="43b6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43b6d-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="43b6d-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="43b6d-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="43b6d-110">Data type:</span></span>  <br/> |<span data-ttu-id="43b6d-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="43b6d-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="43b6d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="43b6d-112">Area:</span></span>  <br/> |<span data-ttu-id="43b6d-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="43b6d-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43b6d-114">備考</span><span class="sxs-lookup"><span data-stu-id="43b6d-114">Remarks</span></span>

<span data-ttu-id="43b6d-115">このプロパティをオブジェクトの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドに渡すことは、表示された表の作成を可能にする[IMAPITable](imapitableiunknown.md)インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="43b6d-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="43b6d-116">MAPI では、このテーブルを使用して、 [IAddrBook::Details](iaddrbook-details.md)の呼び出しへの応答で、アドレス帳のオブジェクトのプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="43b6d-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="43b6d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="43b6d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="43b6d-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="43b6d-118">Header files</span></span>

<span data-ttu-id="43b6d-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43b6d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="43b6d-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="43b6d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="43b6d-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43b6d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="43b6d-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43b6d-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43b6d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="43b6d-123">See also</span></span>



[<span data-ttu-id="43b6d-124">PidTagCreateTemplates の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="43b6d-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="43b6d-125">PidTagSearch の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="43b6d-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="43b6d-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="43b6d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43b6d-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="43b6d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43b6d-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="43b6d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43b6d-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="43b6d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

