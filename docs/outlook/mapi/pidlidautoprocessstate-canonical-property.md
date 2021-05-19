---
title: PidLidAutoProcessState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0918c15d87219c1ee20b177ae21e718e0289cf04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342064"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="90a3d-103">PidLidAutoProcessState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90a3d-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="90a3d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90a3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90a3d-105">電子メール メッセージの自動処理で使用されるオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="90a3d-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90a3d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="90a3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90a3d-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="90a3d-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="90a3d-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="90a3d-108">Property set:</span></span>  <br/> |<span data-ttu-id="90a3d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="90a3d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="90a3d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="90a3d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="90a3d-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="90a3d-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="90a3d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="90a3d-112">Data type:</span></span>  <br/> |<span data-ttu-id="90a3d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="90a3d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="90a3d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="90a3d-114">Area:</span></span>  <br/> |<span data-ttu-id="90a3d-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="90a3d-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90a3d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="90a3d-116">Remarks</span></span>

<span data-ttu-id="90a3d-117">プロパティが存在しない場合、既定値の "0x00000000" が使用されます。</span><span class="sxs-lookup"><span data-stu-id="90a3d-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="90a3d-118">このプロパティを設定する場合は、次の表のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90a3d-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="90a3d-119">**値**</span><span class="sxs-lookup"><span data-stu-id="90a3d-119">**Value**</span></span>|<span data-ttu-id="90a3d-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="90a3d-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90a3d-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90a3d-121">0x00000000</span></span>  <br/> |<span data-ttu-id="90a3d-122">メッセージを自動的に処理しない。</span><span class="sxs-lookup"><span data-stu-id="90a3d-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="90a3d-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="90a3d-123">0x00000001</span></span>  <br/> |<span data-ttu-id="90a3d-124">メッセージを自動的に処理するか、メッセージを開いたときに処理します。</span><span class="sxs-lookup"><span data-stu-id="90a3d-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="90a3d-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="90a3d-125">0x00000002</span></span>  <br/> |<span data-ttu-id="90a3d-126">メッセージを処理できるのは、メッセージを開いた場合のみです。</span><span class="sxs-lookup"><span data-stu-id="90a3d-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="90a3d-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="90a3d-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90a3d-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="90a3d-128">Protocol specifications</span></span>

<span data-ttu-id="90a3d-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90a3d-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90a3d-130">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="90a3d-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90a3d-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90a3d-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90a3d-132">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="90a3d-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90a3d-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="90a3d-133">Header files</span></span>

<span data-ttu-id="90a3d-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90a3d-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="90a3d-135">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="90a3d-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90a3d-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="90a3d-136">See also</span></span>



[<span data-ttu-id="90a3d-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="90a3d-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90a3d-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90a3d-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90a3d-139">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="90a3d-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90a3d-140">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="90a3d-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

