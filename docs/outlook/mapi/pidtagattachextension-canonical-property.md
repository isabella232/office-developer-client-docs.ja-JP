---
title: PidTagAttachExtension 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388431"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="9b4d8-103">PidTagAttachExtension 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9b4d8-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="9b4d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b4d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b4d8-105">添付ファイルのドキュメントの種類を示すファイル名の拡張子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9b4d8-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b4d8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9b4d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b4d8-107">PR_ATTACH_EXTENSION、PR_ATTACH_EXTENSION_A、PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="9b4d8-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="9b4d8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9b4d8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b4d8-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="9b4d8-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="9b4d8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9b4d8-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b4d8-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b4d8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9b4d8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9b4d8-112">Area:</span></span>  <br/> |<span data-ttu-id="9b4d8-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="9b4d8-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b4d8-114">備考</span><span class="sxs-lookup"><span data-stu-id="9b4d8-114">Remarks</span></span>

<span data-ttu-id="9b4d8-115">これらのプロパティは、送信時にクライアント アプリケーションによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="9b4d8-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="9b4d8-116">メッセージング システムで使用されて**PR_ATTACH_EXTENSION**メッセージの添付ファイル (ルートに変換) を変換する場合または受信したメッセージの添付ファイルに基づくアプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="9b4d8-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="9b4d8-117">送信元のクライアントは、これらのプロパティの値を指定しない、する場合、添付ファイルを処理するメッセージ ・ ストアがそれを生成する義務を負いません。</span><span class="sxs-lookup"><span data-stu-id="9b4d8-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="9b4d8-118">受信側のクライアントは、 **PR_ATTACH_EXTENSION**、最初に確認する必要があり。、このオプションを指定しない場合は、ファイル名の拡張子の添付ファイルの**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) **PR_ATTACH_LONG_FILENAME を解析する必要があります。**([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="9b4d8-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9b4d8-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9b4d8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b4d8-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9b4d8-120">Protocol specifications</span></span>

<span data-ttu-id="9b4d8-121">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b4d8-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b4d8-122">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="9b4d8-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b4d8-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9b4d8-123">Header files</span></span>

<span data-ttu-id="9b4d8-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b4d8-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b4d8-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9b4d8-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b4d8-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9b4d8-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9b4d8-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9b4d8-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b4d8-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b4d8-128">See also</span></span>



[<span data-ttu-id="9b4d8-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9b4d8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b4d8-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9b4d8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b4d8-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9b4d8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b4d8-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9b4d8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

