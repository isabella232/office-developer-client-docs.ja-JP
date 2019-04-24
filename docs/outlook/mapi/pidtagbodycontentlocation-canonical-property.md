---
title: PidTagBodyContentLocation 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyContentLocation
api_type:
- HeaderDef
ms.assetid: a66d1c64-5c5a-4980-9acd-72448108fd2c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 90a873174b5b990f165d0b2173efa38fc7df2d9d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350940"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="9215b-103">PidTagBodyContentLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9215b-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="9215b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9215b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9215b-105">MIME コンテンツの場所のヘッダーフィールドの値を格納します。</span><span class="sxs-lookup"><span data-stu-id="9215b-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9215b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9215b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9215b-107">PR_BODY_CONTENT_LOCATION、PR_BODY_CONTENT_LOCATION_A、PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="9215b-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="9215b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9215b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9215b-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="9215b-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="9215b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9215b-110">Data type:</span></span>  <br/> |<span data-ttu-id="9215b-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9215b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9215b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9215b-112">Area:</span></span>  <br/> |<span data-ttu-id="9215b-113">MIME</span><span class="sxs-lookup"><span data-stu-id="9215b-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9215b-114">解説</span><span class="sxs-lookup"><span data-stu-id="9215b-114">Remarks</span></span>

<span data-ttu-id="9215b-115">これらのプロパティの値を設定するには、mime クライアントは、メッセージ本文にマッピングされている mime エンティティのコンテンツの場所ヘッダーフィールドに必要な値を書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="9215b-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="9215b-116">mime リーダーは、このような mime エンティティのコンテンツの場所ヘッダーフィールドの値をこれらのプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9215b-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9215b-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9215b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9215b-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9215b-118">Protocol specifications</span></span>

<span data-ttu-id="9215b-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9215b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9215b-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9215b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9215b-121">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9215b-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9215b-122">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="9215b-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9215b-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9215b-123">Header files</span></span>

<span data-ttu-id="9215b-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9215b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9215b-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9215b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9215b-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9215b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9215b-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9215b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9215b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9215b-128">See also</span></span>



[<span data-ttu-id="9215b-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9215b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9215b-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9215b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9215b-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9215b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9215b-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9215b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

