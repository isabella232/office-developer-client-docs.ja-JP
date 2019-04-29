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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ae9b79abea9a1b2b31867b9ed575e16e8f1c4474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412472"
---
# <a name="pidtagattachmimesequence-canonical-property"></a><span data-ttu-id="166b3-103">PidTagAttachMimeSequence 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="166b3-103">PidTagAttachMimeSequence Canonical Property</span></span>

  
  
<span data-ttu-id="166b3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="166b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="166b3-105">mime メッセージ添付ファイルの mime シーケンス番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="166b3-105">Contains the MIME sequence number of a MIME message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="166b3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="166b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="166b3-107">PR_ATTACH_MIME_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="166b3-107">PR_ATTACH_MIME_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="166b3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="166b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="166b3-109">0x3710</span><span class="sxs-lookup"><span data-stu-id="166b3-109">0x3710</span></span>  <br/> |
|<span data-ttu-id="166b3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="166b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="166b3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="166b3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="166b3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="166b3-112">Area:</span></span>  <br/> |<span data-ttu-id="166b3-113">メッセージ添付ファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="166b3-113">Message Attachment Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="166b3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="166b3-114">Remarks</span></span>

<span data-ttu-id="166b3-115">このプロパティは、MHTML サポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="166b3-115">This property is used for MHTML support.</span></span> <span data-ttu-id="166b3-116">mime メッセージの親 mime マルチパート本体内の添付ファイルのシーケンス番号を表します。</span><span class="sxs-lookup"><span data-stu-id="166b3-116">It represents the sequence number of the attachment within the parent MIME multipart body part of the MIME message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="166b3-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="166b3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="166b3-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="166b3-118">Header files</span></span>

<span data-ttu-id="166b3-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="166b3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="166b3-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="166b3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="166b3-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="166b3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="166b3-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="166b3-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="166b3-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="166b3-123">See also</span></span>



[<span data-ttu-id="166b3-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="166b3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="166b3-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="166b3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="166b3-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="166b3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="166b3-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="166b3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

