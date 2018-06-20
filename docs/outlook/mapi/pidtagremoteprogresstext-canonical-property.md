---
title: PidTagRemoteProgressText の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgressText
api_type:
- COM
ms.assetid: b74d4350-4ad6-4c3f-8326-bd28537dfa0f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c4b4093fd51d781b7226e5d6239a5d894ffe1107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803318"
---
# <a name="pidtagremoteprogresstext-canonical-property"></a><span data-ttu-id="50e66-103">PidTagRemoteProgressText の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="50e66-103">PidTagRemoteProgressText Canonical Property</span></span>

  
  
<span data-ttu-id="50e66-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50e66-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50e66-105">このプロパティには、リモート転送の状態を示す文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50e66-105">This property contains a string that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50e66-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="50e66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50e66-107">PR_REMOTE_PROGRESS_TEXT、PR_REMOTE_PROGRESS_TEXT_A、PR_REMOTE_PROGRESS_TEXT_W</span><span class="sxs-lookup"><span data-stu-id="50e66-107">PR_REMOTE_PROGRESS_TEXT, PR_REMOTE_PROGRESS_TEXT_A, PR_REMOTE_PROGRESS_TEXT_W</span></span>  <br/> |
|<span data-ttu-id="50e66-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="50e66-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50e66-109">0x3E0C</span><span class="sxs-lookup"><span data-stu-id="50e66-109">0x3E0C</span></span>  <br/> |
|<span data-ttu-id="50e66-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="50e66-110">Data type:</span></span>  <br/> |<span data-ttu-id="50e66-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50e66-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="50e66-112">領域:</span><span class="sxs-lookup"><span data-stu-id="50e66-112">Area:</span></span>  <br/> |<span data-ttu-id="50e66-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="50e66-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50e66-114">備考</span><span class="sxs-lookup"><span data-stu-id="50e66-114">Remarks</span></span>

<span data-ttu-id="50e66-115">このテキストに関連付けられている数値コードは、 **PR_REMOTE_PROGRESS** ([PidTagRemoteProgress](pidtagremoteprogress-canonical-property.md)) プロパティに渡されます。</span><span class="sxs-lookup"><span data-stu-id="50e66-115">A numeric code associated with this text is passed in the **PR_REMOTE_PROGRESS** ([PidTagRemoteProgress](pidtagremoteprogress-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50e66-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="50e66-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="50e66-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="50e66-117">Header files</span></span>

<span data-ttu-id="50e66-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50e66-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="50e66-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="50e66-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="50e66-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="50e66-120">Mapitags.h</span></span>
  
> <span data-ttu-id="50e66-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50e66-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50e66-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="50e66-122">See also</span></span>



[<span data-ttu-id="50e66-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50e66-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50e66-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50e66-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50e66-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="50e66-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50e66-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="50e66-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

