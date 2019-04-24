---
title: PidLidFlagRequest 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357807"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="40b50-103">PidLidFlagRequest 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40b50-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="40b50-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40b50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40b50-105">会議出席依頼の状態を表します。</span><span class="sxs-lookup"><span data-stu-id="40b50-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40b50-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="40b50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40b50-107">dispidrequest</span><span class="sxs-lookup"><span data-stu-id="40b50-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="40b50-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="40b50-108">Property set:</span></span>  <br/> |<span data-ttu-id="40b50-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="40b50-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="40b50-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="40b50-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="40b50-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="40b50-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="40b50-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="40b50-112">Data type:</span></span>  <br/> |<span data-ttu-id="40b50-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40b50-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40b50-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="40b50-114">Area:</span></span>  <br/> |<span data-ttu-id="40b50-115">フラグ</span><span class="sxs-lookup"><span data-stu-id="40b50-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40b50-116">解説</span><span class="sxs-lookup"><span data-stu-id="40b50-116">Remarks</span></span>

<span data-ttu-id="40b50-117">Microsoft Office Outlook では、会議出席依頼は予定アイテムです。</span><span class="sxs-lookup"><span data-stu-id="40b50-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="40b50-118">このプロパティには、フラグに関連付けられる specifiable テキストが含まれていますが、メッセージオブジェクトがフラグ付きまたは完了済みであり、会議関連オブジェクトに対して存在してはならない場合に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40b50-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="40b50-119">このプロパティを設定する必要がある場合は、クライアントがこのプロパティをサポートしないようにして、常に "フォローアップ" (必要な場合は、ユーザーの言語に変換されます) を文字列の値として記述します。</span><span class="sxs-lookup"><span data-stu-id="40b50-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="40b50-120">このプロパティは、 **dispidflagstringenum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) プロパティと**dispidvalidflagstringプルーフ**([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) プロパティの値に基づいて、条件付きで無視される必要があります。</span><span class="sxs-lookup"><span data-stu-id="40b50-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40b50-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="40b50-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40b50-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="40b50-122">Protocol specifications</span></span>

<span data-ttu-id="40b50-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40b50-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40b50-124">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="40b50-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40b50-125">[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40b50-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40b50-126">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="40b50-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40b50-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="40b50-127">Header files</span></span>

<span data-ttu-id="40b50-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40b50-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="40b50-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="40b50-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40b50-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="40b50-130">See also</span></span>



[<span data-ttu-id="40b50-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="40b50-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40b50-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40b50-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40b50-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="40b50-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40b50-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="40b50-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

