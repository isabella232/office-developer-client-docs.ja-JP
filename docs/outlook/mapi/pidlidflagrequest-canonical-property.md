---
title: PidLidFlagRequest の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: df2e474206559dadf250bdf9a078c69da61187c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801974"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="e39af-103">PidLidFlagRequest の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e39af-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="e39af-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e39af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e39af-105">会議出席依頼のステータスを表します。</span><span class="sxs-lookup"><span data-stu-id="e39af-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e39af-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e39af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e39af-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="e39af-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="e39af-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e39af-108">Property set:</span></span>  <br/> |<span data-ttu-id="e39af-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e39af-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e39af-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e39af-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e39af-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="e39af-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="e39af-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e39af-112">Data type:</span></span>  <br/> |<span data-ttu-id="e39af-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e39af-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e39af-114">領域:</span><span class="sxs-lookup"><span data-stu-id="e39af-114">Area:</span></span>  <br/> |<span data-ttu-id="e39af-115">フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="e39af-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e39af-116">備考</span><span class="sxs-lookup"><span data-stu-id="e39af-116">Remarks</span></span>

<span data-ttu-id="e39af-117">Microsoft Office Outlook の会議出席依頼は予定アイテムです。</span><span class="sxs-lookup"><span data-stu-id="e39af-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="e39af-118">このプロパティは、フラグに関連付けられるユーザーを指定できるテキストが含まれていて、メッセージ オブジェクトのフラグを設定または完了すると、設定する必要がありますが、会議に関連するオブジェクトが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e39af-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="e39af-119">クライアントの選択せずに、このプロパティをサポートして、常に「フォロー アップ」(該当する場合、ユーザーの言語に翻訳された) を記述を使用する可能性がありますこのプロパティを設定する必要があるときに文字列の値とします。</span><span class="sxs-lookup"><span data-stu-id="e39af-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="e39af-120">このプロパティは、 **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) と**dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) のプロパティの値に基づいて条件付きで無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e39af-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e39af-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e39af-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e39af-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e39af-122">Protocol specifications</span></span>

<span data-ttu-id="e39af-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e39af-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e39af-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e39af-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e39af-125">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e39af-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e39af-126">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e39af-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e39af-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e39af-127">Header files</span></span>

<span data-ttu-id="e39af-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e39af-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e39af-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e39af-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e39af-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e39af-130">See also</span></span>



[<span data-ttu-id="e39af-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e39af-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e39af-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e39af-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e39af-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e39af-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e39af-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e39af-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

