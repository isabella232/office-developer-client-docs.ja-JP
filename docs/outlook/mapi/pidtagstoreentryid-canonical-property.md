---
title: PidTagStoreEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7dc8ea74d36dd8aee4acec426e97d8b5e3ba2234
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392950"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="90bd6-103">PidTagStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90bd6-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="90bd6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90bd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90bd6-105">オブジェクトが格納されているメッセージ ストアの一意のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="90bd6-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90bd6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="90bd6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90bd6-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="90bd6-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="90bd6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="90bd6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90bd6-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="90bd6-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="90bd6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="90bd6-110">Data type:</span></span>  <br/> |<span data-ttu-id="90bd6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="90bd6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="90bd6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="90bd6-112">Area:</span></span>  <br/> |<span data-ttu-id="90bd6-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="90bd6-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90bd6-114">備考</span><span class="sxs-lookup"><span data-stu-id="90bd6-114">Remarks</span></span>

<span data-ttu-id="90bd6-115">[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドを使用してメッセージ ストアを開くには、このプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="90bd6-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="90bd6-116">メッセージ ・ ストアを所有している任意のオブジェクトを開くにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="90bd6-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="90bd6-117">メッセージ ・ ストアのこのプロパティは、ストアの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="90bd6-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="90bd6-118">クライアント アプリケーションは、 [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md)メソッドを使用して 2 つのプロパティを比較できます。</span><span class="sxs-lookup"><span data-stu-id="90bd6-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90bd6-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="90bd6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90bd6-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="90bd6-120">Protocol specifications</span></span>

<span data-ttu-id="90bd6-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90bd6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90bd6-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="90bd6-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90bd6-123">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90bd6-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90bd6-124">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="90bd6-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="90bd6-125">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90bd6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90bd6-126">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="90bd6-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="90bd6-127">[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90bd6-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90bd6-128">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="90bd6-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="90bd6-129">[[MS OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90bd6-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90bd6-130">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="90bd6-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90bd6-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="90bd6-131">Header files</span></span>

<span data-ttu-id="90bd6-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90bd6-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="90bd6-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="90bd6-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="90bd6-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90bd6-134">Mapitags.h</span></span>
  
> <span data-ttu-id="90bd6-135">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="90bd6-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90bd6-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="90bd6-136">See also</span></span>



[<span data-ttu-id="90bd6-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="90bd6-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90bd6-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="90bd6-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90bd6-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="90bd6-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90bd6-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="90bd6-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

