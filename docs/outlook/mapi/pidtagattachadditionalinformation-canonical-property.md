---
title: PidTagAttachAdditionalInformation の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 83de3a4ad7c93b2dfee8063ab63bfbf0724a5f61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802454"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="6df90-103">PidTagAttachAdditionalInformation の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6df90-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="6df90-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6df90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6df90-105">Windows 以外の添付ファイルのファイルの種類の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6df90-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6df90-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6df90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6df90-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="6df90-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="6df90-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6df90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6df90-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="6df90-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="6df90-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6df90-110">Data type:</span></span>  <br/> |<span data-ttu-id="6df90-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6df90-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6df90-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6df90-112">Area:</span></span>  <br/> |<span data-ttu-id="6df90-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="6df90-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6df90-114">備考</span><span class="sxs-lookup"><span data-stu-id="6df90-114">Remarks</span></span>

<span data-ttu-id="6df90-115">このプロパティは、添付ファイルのエンコーディングに基づいて、特定の添付ファイルに関するメタデータを提供します。</span><span class="sxs-lookup"><span data-stu-id="6df90-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="6df90-116">たとえば、 **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) のプロパティには、MacBinary が含まれている、 **PR_ATTACH_ADDITIONAL_INFO**が含まれています、Macintosh のファイルの作成者とファイルの種類を":CREA:TYPE"として書式設定を表す文字列にはエンコード済みの Macintosh のファイルです。</span><span class="sxs-lookup"><span data-stu-id="6df90-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6df90-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6df90-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6df90-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6df90-118">Protocol specifications</span></span>

<span data-ttu-id="6df90-119">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6df90-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6df90-120">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="6df90-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6df90-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6df90-121">Header files</span></span>

<span data-ttu-id="6df90-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6df90-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6df90-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6df90-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6df90-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6df90-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6df90-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6df90-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6df90-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="6df90-126">See also</span></span>



[<span data-ttu-id="6df90-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6df90-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6df90-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6df90-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6df90-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6df90-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6df90-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6df90-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

