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
ms.openlocfilehash: e46a6556b88452fb453b031fc1a90762fd748f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802508"
---
# <a name="pidtagattachmimesequence-canonical-property"></a><span data-ttu-id="51172-103">PidTagAttachMimeSequence 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="51172-103">PidTagAttachMimeSequence Canonical Property</span></span>

  
  
<span data-ttu-id="51172-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51172-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51172-105">MIME メッセージの添付ファイルの MIME のシーケンス番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51172-105">Contains the MIME sequence number of a MIME message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51172-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="51172-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51172-107">PR_ATTACH_MIME_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="51172-107">PR_ATTACH_MIME_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="51172-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="51172-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51172-109">0x3710</span><span class="sxs-lookup"><span data-stu-id="51172-109">0x3710</span></span>  <br/> |
|<span data-ttu-id="51172-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="51172-110">Data type:</span></span>  <br/> |<span data-ttu-id="51172-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="51172-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="51172-112">領域:</span><span class="sxs-lookup"><span data-stu-id="51172-112">Area:</span></span>  <br/> |<span data-ttu-id="51172-113">メッセージの添付ファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="51172-113">Message Attachment Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51172-114">注釈</span><span class="sxs-lookup"><span data-stu-id="51172-114">Remarks</span></span>

<span data-ttu-id="51172-115">このプロパティが使用される MHTML をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="51172-115">This property is used for MHTML support.</span></span> <span data-ttu-id="51172-116">MIME メッセージの MIME のマルチパートのボディ部の親内の添付ファイルのシーケンス番号を表します。</span><span class="sxs-lookup"><span data-stu-id="51172-116">It represents the sequence number of the attachment within the parent MIME multipart body part of the MIME message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51172-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="51172-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="51172-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="51172-118">Header files</span></span>

<span data-ttu-id="51172-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51172-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="51172-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="51172-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="51172-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="51172-121">Mapitags.h</span></span>
  
> <span data-ttu-id="51172-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51172-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51172-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="51172-123">See also</span></span>



[<span data-ttu-id="51172-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="51172-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51172-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="51172-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51172-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="51172-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51172-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="51172-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

