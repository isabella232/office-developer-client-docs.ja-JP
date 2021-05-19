---
title: PidTagDeferredSendNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e3a30dad433b255573e4e3f041e6475b9227a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357737"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="24280-103">PidTagDeferredSendNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="24280-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="24280-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24280-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24280-105">メッセージの送信延期を計算するために使用できる数値を含む。</span><span class="sxs-lookup"><span data-stu-id="24280-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24280-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="24280-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24280-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="24280-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="24280-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="24280-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24280-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="24280-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="24280-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="24280-110">Data type:</span></span>  <br/> |<span data-ttu-id="24280-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="24280-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="24280-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="24280-112">Area:</span></span>  <br/> |<span data-ttu-id="24280-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="24280-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24280-114">注釈</span><span class="sxs-lookup"><span data-stu-id="24280-114">Remarks</span></span>

<span data-ttu-id="24280-115">このプロパティは、存在しない場合PR_DEFERRED_SEND_TIME **(** [PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) プロパティを計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="24280-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="24280-116">メッセージの送信が延期される場合 **、PR_DEFERRED_SEND_NUMBER** プロパティが存在しない場合は **、PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) プロパティと共に **PR_DEFERRED_SEND_TIME PR_DEFERRED_SEND_NUMBER** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24280-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="24280-117">値 **PR_DEFERRED_SEND_NUMBER** 0 ~ 999 の間で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24280-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="24280-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="24280-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24280-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="24280-119">Protocol specifications</span></span>

<span data-ttu-id="24280-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24280-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24280-121">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="24280-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24280-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="24280-122">Header files</span></span>

<span data-ttu-id="24280-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24280-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="24280-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="24280-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="24280-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24280-125">Mapitags.h</span></span>
  
> <span data-ttu-id="24280-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="24280-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24280-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="24280-127">See also</span></span>



[<span data-ttu-id="24280-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="24280-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24280-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="24280-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24280-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="24280-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24280-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="24280-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

