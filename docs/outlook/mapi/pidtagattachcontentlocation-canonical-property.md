---
title: PidTagAttachContentLocation の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d886bf1e30eae6b4b26512eed95988516a609c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802456"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="acb79-103">PidTagAttachContentLocation の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="acb79-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="acb79-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="acb79-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="acb79-105">多目的インターネット メール拡張 (MIME) メッセージの添付ファイルのコンテンツの場所のヘッダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="acb79-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acb79-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="acb79-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="acb79-107">PR_ATTACH_CONTENT_LOCATION、PR_ATTACH_CONTENT_LOCATION_A、PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="acb79-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="acb79-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="acb79-108">Identifier:</span></span>  <br/> |<span data-ttu-id="acb79-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="acb79-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="acb79-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="acb79-110">Data type:</span></span>  <br/> |<span data-ttu-id="acb79-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="acb79-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="acb79-112">領域:</span><span class="sxs-lookup"><span data-stu-id="acb79-112">Area:</span></span>  <br/> |<span data-ttu-id="acb79-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="acb79-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acb79-114">備考</span><span class="sxs-lookup"><span data-stu-id="acb79-114">Remarks</span></span>

<span data-ttu-id="acb79-115">これらのプロパティの使用は、MHTML をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="acb79-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="acb79-116">適切な MIME ボディ部のコンテンツ場所ヘッダーを表します。</span><span class="sxs-lookup"><span data-stu-id="acb79-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="acb79-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="acb79-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="acb79-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="acb79-118">Protocol specifications</span></span>

<span data-ttu-id="acb79-119">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="acb79-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="acb79-120">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="acb79-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="acb79-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="acb79-121">Header files</span></span>

<span data-ttu-id="acb79-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="acb79-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="acb79-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="acb79-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="acb79-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="acb79-124">Mapitags.h</span></span>
  
> <span data-ttu-id="acb79-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="acb79-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="acb79-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="acb79-126">See also</span></span>



[<span data-ttu-id="acb79-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="acb79-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="acb79-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="acb79-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="acb79-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="acb79-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="acb79-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="acb79-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

