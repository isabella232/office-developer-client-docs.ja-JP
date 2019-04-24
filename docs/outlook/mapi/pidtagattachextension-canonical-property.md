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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319762"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="02f8d-103">PidTagAttachExtension 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="02f8d-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="02f8d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02f8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02f8d-105">添付ファイルのドキュメントの種類を示すファイル名拡張子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02f8d-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02f8d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="02f8d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02f8d-107">PR_ATTACH_EXTENSION、PR_ATTACH_EXTENSION_A、PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="02f8d-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="02f8d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="02f8d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02f8d-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="02f8d-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="02f8d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="02f8d-110">Data type:</span></span>  <br/> |<span data-ttu-id="02f8d-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="02f8d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="02f8d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="02f8d-112">Area:</span></span>  <br/> |<span data-ttu-id="02f8d-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="02f8d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02f8d-114">解説</span><span class="sxs-lookup"><span data-stu-id="02f8d-114">Remarks</span></span>

<span data-ttu-id="02f8d-115">これらのプロパティは、送信時にクライアントアプリケーションによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="02f8d-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="02f8d-116">メッセージングシステムは、受信したメッセージ内の添付ファイルに基づいて、メッセージの添付ファイルを変換するとき (ルートの変換)、またはアプリケーションを起動するときに**PR_ATTACH_EXTENSION**を使用します。</span><span class="sxs-lookup"><span data-stu-id="02f8d-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="02f8d-117">送信元クライアントがこれらのプロパティの値を提供していない場合、添付ファイルを処理するメッセージストアは、それを生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="02f8d-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="02f8d-118">受信側クライアントは、まず**PR_ATTACH_EXTENSION**をチェックし、指定されていない場合は、添付ファイルの**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) または PR_ATTACH_LONG_FILENAME からファイル名拡張子を解析する必要があります。 \*\*\*\*([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="02f8d-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02f8d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="02f8d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02f8d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="02f8d-120">Protocol specifications</span></span>

<span data-ttu-id="02f8d-121">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f8d-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02f8d-122">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="02f8d-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02f8d-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="02f8d-123">Header files</span></span>

<span data-ttu-id="02f8d-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02f8d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="02f8d-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="02f8d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="02f8d-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="02f8d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="02f8d-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02f8d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02f8d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="02f8d-128">See also</span></span>



[<span data-ttu-id="02f8d-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="02f8d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02f8d-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="02f8d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02f8d-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="02f8d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02f8d-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="02f8d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

