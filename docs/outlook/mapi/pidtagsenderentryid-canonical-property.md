---
title: PidTagSenderEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEntryId
api_type:
- COM
ms.assetid: 9f311dd2-853e-46f7-966a-c2ab7a1fb6c5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 46ccc3c7e07e6920508fea630c96700d39366a35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803519"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="51857-103">PidTagSenderEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="51857-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="51857-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51857-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51857-105">メッセージ送信者のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51857-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51857-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="51857-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51857-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="51857-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="51857-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="51857-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51857-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="51857-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="51857-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="51857-110">Data type:</span></span>  <br/> |<span data-ttu-id="51857-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="51857-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="51857-112">領域:</span><span class="sxs-lookup"><span data-stu-id="51857-112">Area:</span></span>  <br/> |<span data-ttu-id="51857-113">Address</span><span class="sxs-lookup"><span data-stu-id="51857-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51857-114">注釈</span><span class="sxs-lookup"><span data-stu-id="51857-114">Remarks</span></span>

<span data-ttu-id="51857-115">このプロパティは、メッセージの送信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="51857-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="51857-116">以前の既存の値を反映する必要があることはありませんが、送信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51857-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="51857-117">トランスポート プロバイダーは、任意の送信者アドレスのプロパティを指定しない場合、MAPI スプーラーはメソッドを呼び出して、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)のエントリ id を入力しようとします。</span><span class="sxs-lookup"><span data-stu-id="51857-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="51857-118">場合、識別子が提供されているエントリは、MAPI スプーラーを無効にするこのプロパティに「不明」の文字列に対応する id です。</span><span class="sxs-lookup"><span data-stu-id="51857-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="51857-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="51857-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51857-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="51857-120">Protocol specifications</span></span>

<span data-ttu-id="51857-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51857-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51857-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="51857-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51857-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51857-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51857-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="51857-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="51857-125">[[MS OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51857-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51857-126">RSS 項目を表すための操作のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="51857-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="51857-127">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51857-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51857-128">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="51857-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="51857-129">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51857-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51857-130">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="51857-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="51857-131">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51857-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51857-132">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="51857-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="51857-133">[[MS OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51857-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51857-134">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="51857-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51857-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="51857-135">Header files</span></span>

<span data-ttu-id="51857-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51857-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="51857-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="51857-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="51857-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="51857-138">Mapitags.h</span></span>
  
> <span data-ttu-id="51857-139">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51857-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51857-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="51857-140">See also</span></span>



[<span data-ttu-id="51857-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="51857-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51857-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="51857-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51857-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="51857-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51857-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="51857-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

