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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3794386c4461c90f973e4028132cb8220dfaa19b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426353"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="0f2b7-103">PidTagIpmWastebasketEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0f2b7-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0f2b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f2b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f2b7-105">標準の対人間メッセージ (IPM) 削除済みアイテム フォルダーのエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="0f2b7-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f2b7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0f2b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f2b7-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0f2b7-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0f2b7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0f2b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f2b7-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="0f2b7-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="0f2b7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0f2b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f2b7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0f2b7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0f2b7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0f2b7-112">Area:</span></span>  <br/> |<span data-ttu-id="0f2b7-113">Folder</span><span class="sxs-lookup"><span data-stu-id="0f2b7-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f2b7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0f2b7-114">Remarks</span></span>

<span data-ttu-id="0f2b7-115">クライアント アプリケーションは、削除された対人メッセージを削除済みアイテム フォルダーに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f2b7-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="0f2b7-116">メッセージが既にこのフォルダーにある場合、またはこのプロパティがサポートされていない場合、クライアントはメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f2b7-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0f2b7-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0f2b7-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0f2b7-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0f2b7-118">Header files</span></span>

<span data-ttu-id="0f2b7-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f2b7-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f2b7-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0f2b7-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f2b7-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f2b7-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0f2b7-122">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="0f2b7-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f2b7-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f2b7-123">See also</span></span>



[<span data-ttu-id="0f2b7-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0f2b7-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f2b7-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0f2b7-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f2b7-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0f2b7-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f2b7-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0f2b7-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

