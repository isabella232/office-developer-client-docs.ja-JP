---
title: PidTagDetailsTable 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585788"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="7a7b4-103">PidTagDetailsTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a7b4-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="7a7b4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a7b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a7b4-105">埋め込み表示テーブル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a7b4-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a7b4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7a7b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a7b4-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="7a7b4-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="7a7b4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7a7b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a7b4-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="7a7b4-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="7a7b4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7a7b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a7b4-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="7a7b4-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="7a7b4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7a7b4-112">Area:</span></span>  <br/> |<span data-ttu-id="7a7b4-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="7a7b4-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a7b4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7a7b4-114">Remarks</span></span>

<span data-ttu-id="7a7b4-115">このプロパティをオブジェクトの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドに渡すことは、表示された表の作成を可能にする[IMAPITable](imapitableiunknown.md)インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="7a7b4-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="7a7b4-116">MAPI では、このテーブルを使用して、 [IAddrBook::Details](iaddrbook-details.md)の呼び出しへの応答で、アドレス帳のオブジェクトのプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="7a7b4-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7a7b4-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7a7b4-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7a7b4-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7a7b4-118">Header files</span></span>

<span data-ttu-id="7a7b4-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a7b4-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a7b4-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a7b4-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a7b4-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a7b4-121">Mapitags.h</span></span>
  
> <span data-ttu-id="7a7b4-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a7b4-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a7b4-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a7b4-123">See also</span></span>



[<span data-ttu-id="7a7b4-124">PidTagCreateTemplates 標準プロパティ Property</span><span class="sxs-lookup"><span data-stu-id="7a7b4-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="7a7b4-125">PidTagSearch 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a7b4-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="7a7b4-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a7b4-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a7b4-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a7b4-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a7b4-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7a7b4-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a7b4-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7a7b4-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

