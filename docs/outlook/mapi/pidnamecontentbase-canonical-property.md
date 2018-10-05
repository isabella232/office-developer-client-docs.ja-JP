---
title: PidNameContentBase 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397794"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="95042-103">PidNameContentBase 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="95042-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="95042-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95042-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95042-105">[RFC3282] 内容ベース ヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="95042-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95042-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="95042-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="95042-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="95042-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="95042-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="95042-108">Property set:</span></span>  <br/> |<span data-ttu-id="95042-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="95042-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="95042-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="95042-110">Property name:</span></span>  <br/> |<span data-ttu-id="95042-111">コンテンツ ・ ベース</span><span class="sxs-lookup"><span data-stu-id="95042-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="95042-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="95042-112">Data type:</span></span>  <br/> |<span data-ttu-id="95042-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="95042-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="95042-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="95042-114">Area:</span></span>  <br/> |<span data-ttu-id="95042-115">メール</span><span class="sxs-lookup"><span data-stu-id="95042-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95042-116">備考</span><span class="sxs-lookup"><span data-stu-id="95042-116">Remarks</span></span>

<span data-ttu-id="95042-117">このプロパティの値を設定するのには多目的インターネット メッセージの拡張機能 (MIME) クライアントに書き込まなければなりません目的の値内容ベース ヘッダー フィールドにメッセージの本文にマップされた MIME エンティティ。</span><span class="sxs-lookup"><span data-stu-id="95042-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="95042-118">MIME のリーダーは、このプロパティの値をこのような MIME エンティティのコンテンツ ベースのヘッダー フィールドの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="95042-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="95042-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="95042-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95042-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="95042-120">Protocol specifications</span></span>

<span data-ttu-id="95042-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95042-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95042-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="95042-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="95042-123">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95042-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95042-124">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="95042-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95042-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="95042-125">Header files</span></span>

<span data-ttu-id="95042-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95042-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="95042-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="95042-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95042-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="95042-128">See also</span></span>



[<span data-ttu-id="95042-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="95042-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95042-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="95042-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95042-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="95042-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95042-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="95042-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

