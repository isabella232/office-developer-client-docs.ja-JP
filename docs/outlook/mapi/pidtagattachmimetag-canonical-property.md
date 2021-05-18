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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327245"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="284cf-103">PidTagAttachMimeTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="284cf-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="284cf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="284cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="284cf-105">多目的インターネット メール拡張機能 (MIME) 添付ファイルに関する書式設定情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="284cf-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="284cf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="284cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="284cf-107">PR_ATTACH_MIME_TAG、PR_ATTACH_MIME_TAG_A、PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="284cf-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="284cf-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="284cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="284cf-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="284cf-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="284cf-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="284cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="284cf-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="284cf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="284cf-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="284cf-112">Area:</span></span>  <br/> |<span data-ttu-id="284cf-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="284cf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="284cf-114">注釈</span><span class="sxs-lookup"><span data-stu-id="284cf-114">Remarks</span></span>

<span data-ttu-id="284cf-115">PR_ATTACH_TAG **(** [PidTagAttachTag](pidtagattachtag-canonical-property.md)) プロパティに **値 OID_MIMETAG** が含まれている場合、トランスポート プロバイダーは、添付ファイルの書式設定方法を決定するために、これらのプロパティを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="284cf-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="284cf-116">これらのプロパティは、受信 MIME ヘッダーの Content-type パラメーターからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="284cf-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="284cf-117">文字列の構成は、RFC 1521 ドキュメントで定義されています。</span><span class="sxs-lookup"><span data-stu-id="284cf-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="284cf-118">形式は、アプリケーション/バイナリ、テキスト/プレーンなどの型/サブタイプです。</span><span class="sxs-lookup"><span data-stu-id="284cf-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="284cf-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="284cf-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="284cf-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="284cf-120">Protocol specifications</span></span>

<span data-ttu-id="284cf-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="284cf-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="284cf-122">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="284cf-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="284cf-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="284cf-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="284cf-124">権限で管理されたエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="284cf-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="284cf-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="284cf-125">Header files</span></span>

<span data-ttu-id="284cf-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="284cf-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="284cf-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="284cf-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="284cf-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="284cf-128">Mapitags.h</span></span>
  
> <span data-ttu-id="284cf-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="284cf-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="284cf-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="284cf-130">See also</span></span>



[<span data-ttu-id="284cf-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="284cf-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="284cf-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="284cf-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="284cf-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="284cf-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="284cf-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="284cf-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

