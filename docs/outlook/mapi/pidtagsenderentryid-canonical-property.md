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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0bc8b8bd76d553cc4e12e331e9fe7047ef7aaf4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358913"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="45c0c-103">PidTagSenderEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="45c0c-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="45c0c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45c0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45c0c-105">メッセージ送信者のエントリ識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="45c0c-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45c0c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="45c0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45c0c-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="45c0c-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="45c0c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="45c0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45c0c-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="45c0c-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="45c0c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="45c0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="45c0c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="45c0c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="45c0c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="45c0c-112">Area:</span></span>  <br/> |<span data-ttu-id="45c0c-113">Address</span><span class="sxs-lookup"><span data-stu-id="45c0c-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45c0c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="45c0c-114">Remarks</span></span>

<span data-ttu-id="45c0c-115">このプロパティは、メッセージ送信者のアドレス プロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="45c0c-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="45c0c-116">これは、送信トランスポート プロバイダーによって設定する必要があります。これは、以前に既存の値を伝達する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45c0c-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="45c0c-117">送信側アドレスプロパティを提供しているトランスポート プロバイダーがない場合、MAPI スプーラーは、エントリ識別子の [IMAPISession::QueryIdentity](imapisession-queryidentity.md) メソッドを呼び出して、それらを入力します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="45c0c-118">エントリ識別子が指定されていない場合、MAPI スプーラーは、このプロパティの文字列 "Unknown" に対応する識別子です。</span><span class="sxs-lookup"><span data-stu-id="45c0c-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="45c0c-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="45c0c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45c0c-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="45c0c-120">Protocol specifications</span></span>

<span data-ttu-id="45c0c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c0c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c0c-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45c0c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c0c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c0c-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="45c0c-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c0c-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c0c-126">RSS アイテムを表すプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="45c0c-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c0c-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c0c-128">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="45c0c-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c0c-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c0c-130">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="45c0c-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c0c-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c0c-132">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="45c0c-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c0c-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c0c-134">ポスト オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45c0c-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="45c0c-135">Header files</span></span>

<span data-ttu-id="45c0c-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45c0c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="45c0c-137">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="45c0c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="45c0c-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45c0c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="45c0c-139">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="45c0c-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45c0c-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="45c0c-140">See also</span></span>



[<span data-ttu-id="45c0c-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="45c0c-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45c0c-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="45c0c-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45c0c-143">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="45c0c-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45c0c-144">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="45c0c-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

