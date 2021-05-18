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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6a84e51325fcb60c54c2f6b42af0c26a0efd3382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327238"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="daaff-103">PidTagAttachPayloadClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="daaff-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="daaff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="daaff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="daaff-105">MIME X-Payload-Class ヘッダー フィールドの値を格納します。</span><span class="sxs-lookup"><span data-stu-id="daaff-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="daaff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="daaff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="daaff-107">PR_ATTACH_PAYLOAD_CLASS、PR_ATTACH_PAYLOAD_CLASS_A、PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="daaff-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="daaff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="daaff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="daaff-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="daaff-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="daaff-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="daaff-110">Data type:</span></span>  <br/> |<span data-ttu-id="daaff-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="daaff-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="daaff-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="daaff-112">Area:</span></span>  <br/> |<span data-ttu-id="daaff-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="daaff-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daaff-114">注釈</span><span class="sxs-lookup"><span data-stu-id="daaff-114">Remarks</span></span>

<span data-ttu-id="daaff-115">これらのプロパティの値を設定するには、MIME クライアントは X-Payload-Class ヘッダー フィールドを添付ファイルとして分析される MIME エンティティに書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="daaff-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="daaff-116">MIME リーダーは、このヘッダー フィールドの値を対応するプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="daaff-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="daaff-117">MIME リーダーは、添付ファイルとしてではなく、メッセージまたはメッセージ本文として分析される MIME エンティティに表示される場合、このヘッダー フィールドを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="daaff-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="daaff-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="daaff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="daaff-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="daaff-119">Protocol specifications</span></span>

<span data-ttu-id="daaff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daaff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daaff-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="daaff-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="daaff-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daaff-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daaff-123">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="daaff-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="daaff-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="daaff-124">Header files</span></span>

<span data-ttu-id="daaff-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="daaff-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="daaff-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="daaff-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="daaff-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="daaff-127">Mapitags.h</span></span>
  
> <span data-ttu-id="daaff-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="daaff-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="daaff-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="daaff-129">See also</span></span>



[<span data-ttu-id="daaff-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="daaff-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="daaff-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="daaff-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="daaff-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="daaff-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="daaff-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="daaff-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

