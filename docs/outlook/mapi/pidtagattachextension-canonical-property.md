---
title: PidTagAttachExtension の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4d71a0e26e2043bbaf961ae5096afc5789be36be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802474"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="4da13-103">PidTagAttachExtension の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="4da13-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="4da13-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4da13-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4da13-105">添付ファイルのドキュメントの種類を示すファイル名の拡張子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4da13-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4da13-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="4da13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4da13-107">PR_ATTACH_EXTENSION、PR_ATTACH_EXTENSION_A、PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="4da13-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="4da13-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4da13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4da13-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="4da13-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="4da13-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="4da13-110">Data type:</span></span>  <br/> |<span data-ttu-id="4da13-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4da13-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4da13-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4da13-112">Area:</span></span>  <br/> |<span data-ttu-id="4da13-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="4da13-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4da13-114">備考</span><span class="sxs-lookup"><span data-stu-id="4da13-114">Remarks</span></span>

<span data-ttu-id="4da13-115">これらのプロパティは、送信時にクライアント アプリケーションによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="4da13-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="4da13-116">メッセージング システムで使用されて**PR_ATTACH_EXTENSION**メッセージの添付ファイル (ルートに変換) を変換する場合または受信したメッセージの添付ファイルに基づくアプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="4da13-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="4da13-117">送信元のクライアントは、これらのプロパティの値を指定しない、する場合、添付ファイルを処理するメッセージ ・ ストアがそれを生成する義務を負いません。</span><span class="sxs-lookup"><span data-stu-id="4da13-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="4da13-118">受信側のクライアントは、 **PR_ATTACH_EXTENSION**、最初に確認する必要があり。、このオプションを指定しない場合は、ファイル名の拡張子の添付ファイルの**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) **PR_ATTACH_LONG_FILENAME を解析する必要があります。**([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="4da13-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4da13-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4da13-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4da13-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4da13-120">Protocol specifications</span></span>

<span data-ttu-id="4da13-121">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4da13-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4da13-122">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4da13-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4da13-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4da13-123">Header files</span></span>

<span data-ttu-id="4da13-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4da13-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4da13-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4da13-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4da13-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4da13-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4da13-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4da13-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4da13-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4da13-128">See also</span></span>



[<span data-ttu-id="4da13-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4da13-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4da13-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4da13-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4da13-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="4da13-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4da13-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="4da13-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

