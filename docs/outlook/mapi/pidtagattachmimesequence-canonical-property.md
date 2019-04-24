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
ms.openlocfilehash: ae9b79abea9a1b2b31867b9ed575e16e8f1c4474
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327280"
---
# <a name="pidtagattachmimesequence-canonical-property"></a><span data-ttu-id="22063-103">PidTagAttachMimeSequence 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="22063-103">PidTagAttachMimeSequence Canonical Property</span></span>

  
  
<span data-ttu-id="22063-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22063-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22063-105">mime メッセージ添付ファイルの mime シーケンス番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="22063-105">Contains the MIME sequence number of a MIME message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22063-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="22063-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22063-107">PR_ATTACH_MIME_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="22063-107">PR_ATTACH_MIME_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="22063-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="22063-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22063-109">0x3710</span><span class="sxs-lookup"><span data-stu-id="22063-109">0x3710</span></span>  <br/> |
|<span data-ttu-id="22063-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="22063-110">Data type:</span></span>  <br/> |<span data-ttu-id="22063-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="22063-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="22063-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="22063-112">Area:</span></span>  <br/> |<span data-ttu-id="22063-113">メッセージ添付ファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="22063-113">Message Attachment Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22063-114">解説</span><span class="sxs-lookup"><span data-stu-id="22063-114">Remarks</span></span>

<span data-ttu-id="22063-115">このプロパティは、MHTML サポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="22063-115">This property is used for MHTML support.</span></span> <span data-ttu-id="22063-116">mime メッセージの親 mime マルチパート本体内の添付ファイルのシーケンス番号を表します。</span><span class="sxs-lookup"><span data-stu-id="22063-116">It represents the sequence number of the attachment within the parent MIME multipart body part of the MIME message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22063-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="22063-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="22063-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="22063-118">Header files</span></span>

<span data-ttu-id="22063-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22063-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="22063-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="22063-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="22063-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="22063-121">Mapitags.h</span></span>
  
> <span data-ttu-id="22063-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="22063-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22063-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="22063-123">See also</span></span>



[<span data-ttu-id="22063-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="22063-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22063-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="22063-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22063-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="22063-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22063-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="22063-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

