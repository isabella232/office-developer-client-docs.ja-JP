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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319762"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="bc4a2-103">PidTagAttachExtension 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc4a2-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="bc4a2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc4a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc4a2-105">添付ファイルのドキュメントの種類を示すファイル名の拡張子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bc4a2-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc4a2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bc4a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc4a2-107">PR_ATTACH_EXTENSION、PR_ATTACH_EXTENSION_A、PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="bc4a2-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="bc4a2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bc4a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc4a2-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="bc4a2-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="bc4a2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bc4a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc4a2-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc4a2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bc4a2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bc4a2-112">Area:</span></span>  <br/> |<span data-ttu-id="bc4a2-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="bc4a2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc4a2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bc4a2-114">Remarks</span></span>

<span data-ttu-id="bc4a2-115">これらのプロパティは、申請時にクライアント アプリケーションによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="bc4a2-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="bc4a2-116">メッセージング システムは **、PR_ATTACH_EXTENSION添付** ファイルの変換 (ルート内変換) または受信メッセージの添付ファイルに基づいてアプリケーションを起動するときに、アプリケーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="bc4a2-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="bc4a2-117">送信側クライアントがこれらのプロパティの値を提供しない場合、添付ファイルを処理するメッセージ ストアは、添付ファイルを生成する義務を負う必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc4a2-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="bc4a2-118">受信クライアントは、まず **PR_ATTACH_EXTENSION** をチェックし、指定されていない場合は、添付ファイルの PR_ATTACH_FILENAME ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) プロパティまたは **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) プロパティからファイル名の拡張子を解析する必要があります。 </span><span class="sxs-lookup"><span data-stu-id="bc4a2-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bc4a2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bc4a2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc4a2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bc4a2-120">Protocol specifications</span></span>

<span data-ttu-id="bc4a2-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc4a2-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc4a2-122">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="bc4a2-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc4a2-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bc4a2-123">Header files</span></span>

<span data-ttu-id="bc4a2-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc4a2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc4a2-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bc4a2-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc4a2-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc4a2-126">Mapitags.h</span></span>
  
> <span data-ttu-id="bc4a2-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bc4a2-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc4a2-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc4a2-128">See also</span></span>



[<span data-ttu-id="bc4a2-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bc4a2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc4a2-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc4a2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc4a2-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bc4a2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc4a2-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bc4a2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

