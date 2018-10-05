---
title: PidLidToDoTitle 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397584"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="f0022-103">PidLidToDoTitle 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0022-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="f0022-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0022-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0022-105">統合の to do リストでは、このメッセージ オブジェクトを識別するユーザーを指定できるテキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0022-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0022-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f0022-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0022-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="f0022-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="f0022-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f0022-108">Property set:</span></span>  <br/> |<span data-ttu-id="f0022-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f0022-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f0022-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f0022-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f0022-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="f0022-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="f0022-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f0022-112">Data type:</span></span>  <br/> |<span data-ttu-id="f0022-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0022-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f0022-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="f0022-114">Area:</span></span>  <br/> |<span data-ttu-id="f0022-115">タスク</span><span class="sxs-lookup"><span data-stu-id="f0022-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0022-116">備考</span><span class="sxs-lookup"><span data-stu-id="f0022-116">Remarks</span></span>

<span data-ttu-id="f0022-117">タスクでこのプロパティを設定しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0022-117">This property must not be set on a task.</span></span> <span data-ttu-id="f0022-118">空のプロパティを指定するには、長さ 0 の文字列にこのプロパティを設定しないでが代わりにそれを削除します。</span><span class="sxs-lookup"><span data-stu-id="f0022-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="f0022-119">メッセージ オブジェクト、およびプロパティのフラグを付けることが存在しない場合、クライアントは、このプロパティに**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) の値を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0022-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="f0022-120">統合の to do リストでこのプロパティが存在しない場合、クライアント置き換える必要があります**PR_NORMALIZED_SUBJECT**プロパティの値を to do リストにこのプロパティを表示するときです。</span><span class="sxs-lookup"><span data-stu-id="f0022-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="f0022-121">下書きメッセージ オブジェクトでは、[クライアントは、送信者のフラグを実装している場合このプロパティは、 **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) と同じ値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0022-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f0022-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f0022-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0022-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f0022-123">Protocol specifications</span></span>

<span data-ttu-id="f0022-124">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0022-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0022-125">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0022-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="f0022-126">[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0022-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0022-127">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0022-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0022-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f0022-128">Header files</span></span>

<span data-ttu-id="f0022-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0022-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0022-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0022-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0022-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0022-131">See also</span></span>



[<span data-ttu-id="f0022-132">PidTagNormalizedSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0022-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="f0022-133">PidLidFlagRequest ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="f0022-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="f0022-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0022-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0022-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0022-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0022-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0022-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0022-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0022-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

