---
title: PidTagAttachMimeTag の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6f65d67903fa9ebb255345f8666cd53de5512cab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802491"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="243b3-103">PidTagAttachMimeTag の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="243b3-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="243b3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="243b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="243b3-105">多目的インターネット メール拡張 (MIME) の添付文書に関する書式情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="243b3-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="243b3-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="243b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="243b3-107">PR_ATTACH_MIME_TAG、PR_ATTACH_MIME_TAG_A、PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="243b3-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="243b3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="243b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="243b3-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="243b3-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="243b3-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="243b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="243b3-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="243b3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="243b3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="243b3-112">Area:</span></span>  <br/> |<span data-ttu-id="243b3-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="243b3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="243b3-114">備考</span><span class="sxs-lookup"><span data-stu-id="243b3-114">Remarks</span></span>

<span data-ttu-id="243b3-115">**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) のプロパティに**OID_MIMETAG**の値が含まれている場合、トランスポート プロバイダーはこれらのプロパティは、添付ファイルの書式を設定する方法を決定するのにを見てください。</span><span class="sxs-lookup"><span data-stu-id="243b3-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="243b3-116">これらのプロパティは、受信 MIME ヘッダーのコンテンツ タイプのパラメーターからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="243b3-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="243b3-117">文字列の構成は、RFC 1521 ドキュメントで定義されます。</span><span class="sxs-lookup"><span data-stu-id="243b3-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="243b3-118">形式は、アプリケーション/バイナリまたはテキスト/形式などは、タイプ/サブタイプです。</span><span class="sxs-lookup"><span data-stu-id="243b3-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="243b3-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="243b3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="243b3-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="243b3-120">Protocol specifications</span></span>

<span data-ttu-id="243b3-121">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="243b3-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="243b3-122">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="243b3-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="243b3-123">[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="243b3-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="243b3-124">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="243b3-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="243b3-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="243b3-125">Header files</span></span>

<span data-ttu-id="243b3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="243b3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="243b3-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="243b3-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="243b3-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="243b3-128">Mapitags.h</span></span>
  
> <span data-ttu-id="243b3-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="243b3-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="243b3-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="243b3-130">See also</span></span>



[<span data-ttu-id="243b3-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="243b3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="243b3-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="243b3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="243b3-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="243b3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="243b3-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="243b3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

