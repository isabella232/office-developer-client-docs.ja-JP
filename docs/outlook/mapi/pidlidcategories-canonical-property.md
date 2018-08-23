---
title: PidLidCategories 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6893afa11cc08b335b0ffb39b725e26478dae22f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574840"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="cdc3c-103">PidLidCategories 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdc3c-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="cdc3c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdc3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdc3c-105">アイテムのカテゴリの一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cdc3c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cdc3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cdc3c-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="cdc3c-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="cdc3c-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-108">Property set:</span></span>  <br/> |<span data-ttu-id="cdc3c-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="cdc3c-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="cdc3c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="cdc3c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cdc3c-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="cdc3c-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="cdc3c-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cdc3c-112">Data type:</span></span>  <br/> |<span data-ttu-id="cdc3c-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cdc3c-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cdc3c-114">領域:</span><span class="sxs-lookup"><span data-stu-id="cdc3c-114">Area:</span></span>  <br/> |<span data-ttu-id="cdc3c-115">Common</span><span class="sxs-lookup"><span data-stu-id="cdc3c-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdc3c-116">注釈</span><span class="sxs-lookup"><span data-stu-id="cdc3c-116">Remarks</span></span>

<span data-ttu-id="cdc3c-117">キーワード ヘッダー フィールドを生成するには、クライアントは、目的の値にこのプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="cdc3c-118">このプロパティは、複数の文字列です。各カテゴリは、1 つのキーワードにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="cdc3c-119">多目的インターネット メール拡張 (MIME) の作成者は、[キーワード] ヘッダー フィールドの (U + 002 C) コンマとスペース (U + 0020) に分離することで別のキーワードをこのプロパティの各部分の値をコピーする必要がありますそれぞれのキーワードです。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="cdc3c-120">MIME ライターは、さまざまな組織内のカテゴリの別のセットの間に競合を避けるために、[キーワード] ヘッダー フィールドにコピーすることではなく、このプロパティを削除可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cdc3c-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cdc3c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cdc3c-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cdc3c-122">Protocol specifications</span></span>

<span data-ttu-id="cdc3c-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdc3c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdc3c-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cdc3c-125">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdc3c-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdc3c-126">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cdc3c-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cdc3c-127">Header files</span></span>

<span data-ttu-id="cdc3c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cdc3c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="cdc3c-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdc3c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cdc3c-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="cdc3c-130">See also</span></span>



[<span data-ttu-id="cdc3c-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdc3c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cdc3c-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdc3c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cdc3c-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cdc3c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cdc3c-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cdc3c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

