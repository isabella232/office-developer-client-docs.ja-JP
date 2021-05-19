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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344976"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="f8294-103">PidLidCategories 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8294-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="f8294-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8294-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8294-105">アイテムのカテゴリの一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8294-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8294-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f8294-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8294-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="f8294-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="f8294-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="f8294-108">Property set:</span></span>  <br/> |<span data-ttu-id="f8294-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="f8294-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="f8294-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f8294-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f8294-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="f8294-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="f8294-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f8294-112">Data type:</span></span>  <br/> |<span data-ttu-id="f8294-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8294-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f8294-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="f8294-114">Area:</span></span>  <br/> |<span data-ttu-id="f8294-115">共通</span><span class="sxs-lookup"><span data-stu-id="f8294-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8294-116">注釈</span><span class="sxs-lookup"><span data-stu-id="f8294-116">Remarks</span></span>

<span data-ttu-id="f8294-117">キーワード ヘッダー フィールドを生成するには、クライアントは、このプロパティの値を目的の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8294-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="f8294-118">このプロパティには複数の文字列があります。各カテゴリは 1 つのキーワードにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8294-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="f8294-119">多目的インターネット メール拡張機能 (MIME) ライターは、このプロパティの各サブ値を[キーワード] ヘッダー フィールドの個別のキーワードにコピーし、各キーワードをコンマ (U+002C) とスペース (U+0020) で区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8294-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="f8294-120">MIME ライターは、異なる組織の異なるカテゴリ セット間の競合を回避するために、このプロパティをキーワード ヘッダー フィールドにコピーする代わりに、このプロパティを削除できます。</span><span class="sxs-lookup"><span data-stu-id="f8294-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f8294-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f8294-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8294-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f8294-122">Protocol specifications</span></span>

<span data-ttu-id="f8294-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8294-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8294-124">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="f8294-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8294-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8294-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8294-126">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="f8294-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8294-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f8294-127">Header files</span></span>

<span data-ttu-id="f8294-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8294-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8294-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f8294-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8294-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8294-130">See also</span></span>



[<span data-ttu-id="f8294-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f8294-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8294-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8294-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8294-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f8294-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8294-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f8294-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

