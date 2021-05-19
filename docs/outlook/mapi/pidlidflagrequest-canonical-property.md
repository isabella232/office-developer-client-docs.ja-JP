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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357807"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="77a13-103">PidLidFlagRequest 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="77a13-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="77a13-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77a13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77a13-105">会議出席依頼の状態を表します。</span><span class="sxs-lookup"><span data-stu-id="77a13-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77a13-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="77a13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77a13-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="77a13-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="77a13-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="77a13-108">Property set:</span></span>  <br/> |<span data-ttu-id="77a13-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="77a13-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="77a13-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="77a13-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="77a13-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="77a13-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="77a13-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="77a13-112">Data type:</span></span>  <br/> |<span data-ttu-id="77a13-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="77a13-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="77a13-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="77a13-114">Area:</span></span>  <br/> |<span data-ttu-id="77a13-115">フラグを設定する</span><span class="sxs-lookup"><span data-stu-id="77a13-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77a13-116">注釈</span><span class="sxs-lookup"><span data-stu-id="77a13-116">Remarks</span></span>

<span data-ttu-id="77a13-117">このMicrosoft Office Outlook、会議出席依頼は予定アイテムです。</span><span class="sxs-lookup"><span data-stu-id="77a13-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="77a13-118">このプロパティには、フラグに関連付けられるユーザー指定可能なテキストが含まれているので、メッセージ オブジェクトにフラグが設定されている場合や完了した場合に設定する必要がありますが、会議関連オブジェクトには存在しません。</span><span class="sxs-lookup"><span data-stu-id="77a13-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="77a13-119">クライアントは、このプロパティをサポートしない選択をし、このプロパティを設定する必要がある場合は、常に "Follow up" (必要に応じてユーザーの言語に翻訳) を文字列の値として記述できます。</span><span class="sxs-lookup"><span data-stu-id="77a13-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="77a13-120">このプロパティは **、dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) プロパティと **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) プロパティの値に基づいて条件付きで無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77a13-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="77a13-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="77a13-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="77a13-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="77a13-122">Protocol specifications</span></span>

<span data-ttu-id="77a13-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77a13-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77a13-124">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="77a13-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="77a13-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77a13-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77a13-126">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="77a13-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="77a13-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="77a13-127">Header files</span></span>

<span data-ttu-id="77a13-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77a13-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="77a13-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="77a13-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77a13-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="77a13-130">See also</span></span>



[<span data-ttu-id="77a13-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="77a13-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77a13-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="77a13-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77a13-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="77a13-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77a13-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="77a13-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

