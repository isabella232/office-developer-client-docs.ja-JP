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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339943"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="75109-103">PidLidToDoTitle 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75109-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="75109-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75109-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75109-105">統合された to-do リストでこのメッセージ オブジェクトを識別するためのユーザー指定可能なテキストが含まれる。</span><span class="sxs-lookup"><span data-stu-id="75109-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75109-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="75109-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75109-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="75109-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="75109-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="75109-108">Property set:</span></span>  <br/> |<span data-ttu-id="75109-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="75109-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="75109-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="75109-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="75109-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="75109-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="75109-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="75109-112">Data type:</span></span>  <br/> |<span data-ttu-id="75109-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="75109-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="75109-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="75109-114">Area:</span></span>  <br/> |<span data-ttu-id="75109-115">タスク</span><span class="sxs-lookup"><span data-stu-id="75109-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75109-116">注釈</span><span class="sxs-lookup"><span data-stu-id="75109-116">Remarks</span></span>

<span data-ttu-id="75109-117">このプロパティは、タスクで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75109-117">This property must not be set on a task.</span></span> <span data-ttu-id="75109-118">空のプロパティを指定するには、このプロパティを長さ 0 の文字列に設定するのではなく、削除します。</span><span class="sxs-lookup"><span data-stu-id="75109-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="75109-119">メッセージ オブジェクトにフラグを設定し、プロパティが存在しない場合、クライアントは **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) の値をこのプロパティに書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="75109-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="75109-120">統合 To Do リストで、このプロパティが存在しない場合、クライアントは、このプロパティを to-do リストに表示 **するときに PR_NORMALIZED_SUBJECT** プロパティの値を置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="75109-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="75109-121">下書きメッセージ オブジェクトで、クライアントが送信者フラグを実装する場合、このプロパティは **dispidRequest** ([PidLidFlagRequest)](pidlidflagrequest-canonical-property.md)と同じ値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75109-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75109-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="75109-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75109-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="75109-123">Protocol specifications</span></span>

<span data-ttu-id="75109-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75109-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75109-125">関連するプロトコル仕様に対するプロパティ セットの定義Exchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="75109-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="75109-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75109-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75109-127">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="75109-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75109-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="75109-128">Header files</span></span>

<span data-ttu-id="75109-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75109-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="75109-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="75109-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75109-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="75109-131">See also</span></span>



[<span data-ttu-id="75109-132">PidTagNormalizedSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75109-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="75109-133">PidLidFlagRequest ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="75109-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="75109-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="75109-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75109-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75109-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75109-136">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="75109-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75109-137">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="75109-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

