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
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344976"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="22cb2-103">PidLidCategories 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="22cb2-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="22cb2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22cb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22cb2-105">アイテムのカテゴリのリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="22cb2-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22cb2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="22cb2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22cb2-107">dispidcategories</span><span class="sxs-lookup"><span data-stu-id="22cb2-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="22cb2-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="22cb2-108">Property set:</span></span>  <br/> |<span data-ttu-id="22cb2-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="22cb2-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="22cb2-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="22cb2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="22cb2-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="22cb2-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="22cb2-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="22cb2-112">Data type:</span></span>  <br/> |<span data-ttu-id="22cb2-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="22cb2-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="22cb2-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="22cb2-114">Area:</span></span>  <br/> |<span data-ttu-id="22cb2-115">共通</span><span class="sxs-lookup"><span data-stu-id="22cb2-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22cb2-116">解説</span><span class="sxs-lookup"><span data-stu-id="22cb2-116">Remarks</span></span>

<span data-ttu-id="22cb2-117">キーワードヘッダーフィールドを生成するには、クライアントはこのプロパティの値を目的の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22cb2-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="22cb2-118">このプロパティには複数の文字列が含まれています。各カテゴリは1つのキーワードにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="22cb2-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="22cb2-119">マルチパーパスインターネットメール内線 (MIME) ライターは、このプロパティの各サブ値をキーワードヘッダーフィールド内の個別のキーワードにコピーします。コンマ (u + 002c) とスペース (u + 0020) で各キーワードを区切ります。</span><span class="sxs-lookup"><span data-stu-id="22cb2-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="22cb2-120">MIME ライターは、異なる組織で異なるカテゴリのセット間の競合を回避するために、このプロパティをキーワードヘッダーフィールドにコピーするのではなく削除することがあります。</span><span class="sxs-lookup"><span data-stu-id="22cb2-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22cb2-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="22cb2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22cb2-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="22cb2-122">Protocol specifications</span></span>

<span data-ttu-id="22cb2-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22cb2-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22cb2-124">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="22cb2-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22cb2-125">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22cb2-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22cb2-126">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="22cb2-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22cb2-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="22cb2-127">Header files</span></span>

<span data-ttu-id="22cb2-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22cb2-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="22cb2-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="22cb2-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22cb2-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="22cb2-130">See also</span></span>



[<span data-ttu-id="22cb2-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="22cb2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22cb2-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="22cb2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22cb2-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="22cb2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22cb2-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="22cb2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

