---
title: PidTagAttachMimeSequence 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeSequence
api_type:
- HeaderDef
ms.assetid: d2a84f24-b4a5-4e16-9219-7a579a31a8f8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b8fe0dd61247d3473db4cc728ecfa2c83682b691
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587720"
---
# <a name="pidtagattachmimesequence-canonical-property"></a><span data-ttu-id="fbac2-103">PidTagAttachMimeSequence 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fbac2-103">PidTagAttachMimeSequence Canonical Property</span></span>

  
  
<span data-ttu-id="fbac2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbac2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbac2-105">MIME メッセージの添付ファイルの MIME のシーケンス番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fbac2-105">Contains the MIME sequence number of a MIME message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbac2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fbac2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fbac2-107">PR_ATTACH_MIME_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="fbac2-107">PR_ATTACH_MIME_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="fbac2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fbac2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fbac2-109">0x3710</span><span class="sxs-lookup"><span data-stu-id="fbac2-109">0x3710</span></span>  <br/> |
|<span data-ttu-id="fbac2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fbac2-110">Data type:</span></span>  <br/> |<span data-ttu-id="fbac2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fbac2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fbac2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="fbac2-112">Area:</span></span>  <br/> |<span data-ttu-id="fbac2-113">メッセージの添付ファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="fbac2-113">Message Attachment Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbac2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fbac2-114">Remarks</span></span>

<span data-ttu-id="fbac2-115">このプロパティが使用される MHTML をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="fbac2-115">This property is used for MHTML support.</span></span> <span data-ttu-id="fbac2-116">MIME メッセージの MIME のマルチパートのボディ部の親内の添付ファイルのシーケンス番号を表します。</span><span class="sxs-lookup"><span data-stu-id="fbac2-116">It represents the sequence number of the attachment within the parent MIME multipart body part of the MIME message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fbac2-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fbac2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fbac2-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fbac2-118">Header files</span></span>

<span data-ttu-id="fbac2-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fbac2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="fbac2-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fbac2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="fbac2-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fbac2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="fbac2-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fbac2-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fbac2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="fbac2-123">See also</span></span>



[<span data-ttu-id="fbac2-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fbac2-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fbac2-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fbac2-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fbac2-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fbac2-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fbac2-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fbac2-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

