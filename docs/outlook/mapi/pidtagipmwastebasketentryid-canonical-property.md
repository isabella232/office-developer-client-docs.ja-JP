---
title: PidTagIpmWastebasketEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b9b8cff0a552c5c12108bdc4b31fe9c3930ab5d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802930"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="f0dc2-103">PidTagIpmWastebasketEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0dc2-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f0dc2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0dc2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0dc2-105">標準的な個人間メッセージ (IPM) の [削除済みアイテム フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0dc2-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0dc2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f0dc2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0dc2-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f0dc2-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f0dc2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f0dc2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0dc2-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="f0dc2-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="f0dc2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f0dc2-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0dc2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f0dc2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f0dc2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f0dc2-112">Area:</span></span>  <br/> |<span data-ttu-id="f0dc2-113">Folder</span><span class="sxs-lookup"><span data-stu-id="f0dc2-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0dc2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f0dc2-114">Remarks</span></span>

<span data-ttu-id="f0dc2-115">クライアント アプリケーションは、個人間のメッセージを削除を削除済みアイテム フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="f0dc2-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="f0dc2-116">このフォルダーにメッセージがある場合、またはこのプロパティがサポートされていない場合は、クライアントはメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0dc2-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f0dc2-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f0dc2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f0dc2-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f0dc2-118">Header files</span></span>

<span data-ttu-id="f0dc2-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0dc2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0dc2-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0dc2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0dc2-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f0dc2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f0dc2-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0dc2-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0dc2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0dc2-123">See also</span></span>



[<span data-ttu-id="f0dc2-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0dc2-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0dc2-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0dc2-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0dc2-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0dc2-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0dc2-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0dc2-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

