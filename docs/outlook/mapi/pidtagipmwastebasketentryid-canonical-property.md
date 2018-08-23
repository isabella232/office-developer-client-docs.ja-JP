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
ms.openlocfilehash: 66bbf49d737c42ecc2f6c765a60540163649f447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573895"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="87501-103">PidTagIpmWastebasketEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="87501-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="87501-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87501-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87501-105">標準的な個人間メッセージ (IPM) の [削除済みアイテム フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="87501-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87501-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="87501-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87501-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="87501-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="87501-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="87501-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87501-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="87501-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="87501-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="87501-110">Data type:</span></span>  <br/> |<span data-ttu-id="87501-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="87501-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="87501-112">領域:</span><span class="sxs-lookup"><span data-stu-id="87501-112">Area:</span></span>  <br/> |<span data-ttu-id="87501-113">Folder</span><span class="sxs-lookup"><span data-stu-id="87501-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87501-114">注釈</span><span class="sxs-lookup"><span data-stu-id="87501-114">Remarks</span></span>

<span data-ttu-id="87501-115">クライアント アプリケーションは、個人間のメッセージを削除を削除済みアイテム フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="87501-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="87501-116">このフォルダーにメッセージがある場合、またはこのプロパティがサポートされていない場合は、クライアントはメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87501-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="87501-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="87501-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="87501-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="87501-118">Header files</span></span>

<span data-ttu-id="87501-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87501-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="87501-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="87501-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="87501-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="87501-121">Mapitags.h</span></span>
  
> <span data-ttu-id="87501-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="87501-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87501-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="87501-123">See also</span></span>



[<span data-ttu-id="87501-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="87501-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87501-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="87501-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87501-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="87501-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87501-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="87501-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

