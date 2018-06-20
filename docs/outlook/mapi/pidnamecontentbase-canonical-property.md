---
title: PidNameContentBase の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 21469b944bb2ce5db0576e40012335d89d48cb49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802359"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="57a3d-103">PidNameContentBase の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="57a3d-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="57a3d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="57a3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="57a3d-105">[RFC3282] 内容ベース ヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="57a3d-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="57a3d-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="57a3d-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="57a3d-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="57a3d-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="57a3d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="57a3d-108">Property set:</span></span>  <br/> |<span data-ttu-id="57a3d-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="57a3d-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="57a3d-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="57a3d-110">Property name:</span></span>  <br/> |<span data-ttu-id="57a3d-111">コンテンツ ・ ベース</span><span class="sxs-lookup"><span data-stu-id="57a3d-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="57a3d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="57a3d-112">Data type:</span></span>  <br/> |<span data-ttu-id="57a3d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="57a3d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="57a3d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="57a3d-114">Area:</span></span>  <br/> |<span data-ttu-id="57a3d-115">Email</span><span class="sxs-lookup"><span data-stu-id="57a3d-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57a3d-116">備考</span><span class="sxs-lookup"><span data-stu-id="57a3d-116">Remarks</span></span>

<span data-ttu-id="57a3d-117">このプロパティの値を設定するのには多目的インターネット メッセージの拡張機能 (MIME) クライアントに書き込まなければなりません目的の値内容ベース ヘッダー フィールドにメッセージの本文にマップされた MIME エンティティ。</span><span class="sxs-lookup"><span data-stu-id="57a3d-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="57a3d-118">MIME のリーダーは、このプロパティの値をこのような MIME エンティティのコンテンツ ベースのヘッダー フィールドの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="57a3d-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="57a3d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="57a3d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="57a3d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="57a3d-120">Protocol specifications</span></span>

<span data-ttu-id="57a3d-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57a3d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57a3d-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="57a3d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="57a3d-123">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57a3d-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57a3d-124">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="57a3d-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="57a3d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="57a3d-125">Header files</span></span>

<span data-ttu-id="57a3d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57a3d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="57a3d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="57a3d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57a3d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="57a3d-128">See also</span></span>



[<span data-ttu-id="57a3d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="57a3d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57a3d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="57a3d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57a3d-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="57a3d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57a3d-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="57a3d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

