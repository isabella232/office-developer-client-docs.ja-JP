---
title: PidTagAttachPayloadClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d00c1823ba152c20be213f16fe4e3ea3c771a83a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574322"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="6f7d5-103">PidTagAttachPayloadClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f7d5-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="6f7d5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f7d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f7d5-105">MIME X ・ ペイロード ・ クラスのヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f7d5-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f7d5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6f7d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f7d5-107">PR_ATTACH_PAYLOAD_CLASS、PR_ATTACH_PAYLOAD_CLASS_A、PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="6f7d5-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="6f7d5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6f7d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f7d5-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="6f7d5-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="6f7d5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6f7d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f7d5-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f7d5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6f7d5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6f7d5-112">Area:</span></span>  <br/> |<span data-ttu-id="6f7d5-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6f7d5-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f7d5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6f7d5-114">Remarks</span></span>

<span data-ttu-id="6f7d5-115">これらのプロパティの値を設定するのには MIME クライアントは、添付ファイルとして解析される MIME エンティティに X ・ ペイロード ・ クラスのヘッダー フィールドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f7d5-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="6f7d5-116">MIME のリーダーでは、このヘッダー フィールドの値を対応するプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f7d5-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="6f7d5-117">MIME のリーダーは、添付ファイルとしてではなく、メッセージまたはメッセージの本文として分析する MIME エンティティ上に表示されるとき、このヘッダー フィールドを無視してください。</span><span class="sxs-lookup"><span data-stu-id="6f7d5-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f7d5-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6f7d5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f7d5-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6f7d5-119">Protocol specifications</span></span>

<span data-ttu-id="6f7d5-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f7d5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f7d5-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f7d5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f7d5-122">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f7d5-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f7d5-123">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="6f7d5-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f7d5-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6f7d5-124">Header files</span></span>

<span data-ttu-id="6f7d5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f7d5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f7d5-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f7d5-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f7d5-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f7d5-127">Mapitags.h</span></span>
  
> <span data-ttu-id="6f7d5-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f7d5-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f7d5-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f7d5-129">See also</span></span>



[<span data-ttu-id="6f7d5-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f7d5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f7d5-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f7d5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f7d5-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6f7d5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f7d5-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6f7d5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

