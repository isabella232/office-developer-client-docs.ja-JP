---
title: PidTagAttachMimeTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389100"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="08ce0-103">PidTagAttachMimeTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08ce0-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="08ce0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08ce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08ce0-105">多目的インターネット メール拡張 (MIME) の添付文書に関する書式情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="08ce0-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08ce0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="08ce0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08ce0-107">PR_ATTACH_MIME_TAG、PR_ATTACH_MIME_TAG_A、PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="08ce0-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="08ce0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="08ce0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08ce0-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="08ce0-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="08ce0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="08ce0-110">Data type:</span></span>  <br/> |<span data-ttu-id="08ce0-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08ce0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="08ce0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="08ce0-112">Area:</span></span>  <br/> |<span data-ttu-id="08ce0-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="08ce0-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08ce0-114">備考</span><span class="sxs-lookup"><span data-stu-id="08ce0-114">Remarks</span></span>

<span data-ttu-id="08ce0-115">**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) のプロパティに**OID_MIMETAG**の値が含まれている場合、トランスポート プロバイダーはこれらのプロパティは、添付ファイルの書式を設定する方法を決定するのにを見てください。</span><span class="sxs-lookup"><span data-stu-id="08ce0-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="08ce0-116">これらのプロパティは、受信 MIME ヘッダーのコンテンツ タイプのパラメーターからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="08ce0-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="08ce0-117">文字列の構成は、RFC 1521 ドキュメントで定義されます。</span><span class="sxs-lookup"><span data-stu-id="08ce0-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="08ce0-118">形式は、アプリケーション/バイナリまたはテキスト/形式などは、タイプ/サブタイプです。</span><span class="sxs-lookup"><span data-stu-id="08ce0-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08ce0-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="08ce0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08ce0-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="08ce0-120">Protocol specifications</span></span>

<span data-ttu-id="08ce0-121">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08ce0-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08ce0-122">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="08ce0-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="08ce0-123">[[MS OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08ce0-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08ce0-124">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="08ce0-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08ce0-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="08ce0-125">Header files</span></span>

<span data-ttu-id="08ce0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08ce0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="08ce0-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="08ce0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="08ce0-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08ce0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="08ce0-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="08ce0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08ce0-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="08ce0-130">See also</span></span>



[<span data-ttu-id="08ce0-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="08ce0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08ce0-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="08ce0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08ce0-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="08ce0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08ce0-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="08ce0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

