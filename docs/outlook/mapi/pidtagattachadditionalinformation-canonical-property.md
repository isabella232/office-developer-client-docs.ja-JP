---
title: PidTagAttachAdditionalInformation 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339874"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="d75d6-103">PidTagAttachAdditionalInformation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d75d6-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="d75d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d75d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d75d6-105">非添付ファイルのファイルの種類情報Windowsします。</span><span class="sxs-lookup"><span data-stu-id="d75d6-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d75d6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d75d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d75d6-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="d75d6-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="d75d6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d75d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d75d6-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="d75d6-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="d75d6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d75d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="d75d6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d75d6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d75d6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d75d6-112">Area:</span></span>  <br/> |<span data-ttu-id="d75d6-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="d75d6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d75d6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d75d6-114">Remarks</span></span>

<span data-ttu-id="d75d6-115">このプロパティは、添付ファイルのエンコードに基づいて、特定の添付ファイルに関するメタデータを提供します。</span><span class="sxs-lookup"><span data-stu-id="d75d6-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="d75d6-116">たとえば **、PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) プロパティに MacBinary が含まれている場合 **、PR_ATTACH_ADDITIONAL_INFO** には、エンコードされた Macintosh ファイルの ":CREA:TYPE" 形式の Macintosh ファイル作成者とファイルの種類を表す文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d75d6-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d75d6-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d75d6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d75d6-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d75d6-118">Protocol specifications</span></span>

<span data-ttu-id="d75d6-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d75d6-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d75d6-120">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="d75d6-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d75d6-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d75d6-121">Header files</span></span>

<span data-ttu-id="d75d6-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d75d6-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="d75d6-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d75d6-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="d75d6-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d75d6-124">Mapitags.h</span></span>
  
> <span data-ttu-id="d75d6-125">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d75d6-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d75d6-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="d75d6-126">See also</span></span>



[<span data-ttu-id="d75d6-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d75d6-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d75d6-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d75d6-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d75d6-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d75d6-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d75d6-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d75d6-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

