---
title: PidTagContentCorrelator 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6398acf71e62157cf5a6eb7e6caf22130fa9f9d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568806"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="f2cc7-103">PidTagContentCorrelator 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2cc7-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="f2cc7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2cc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2cc7-105">元のメッセージを含むレポートを一致するようにメッセージの送信者を使用できる値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f2cc7-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2cc7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f2cc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2cc7-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="f2cc7-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="f2cc7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f2cc7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2cc7-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="f2cc7-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="f2cc7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f2cc7-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2cc7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f2cc7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f2cc7-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f2cc7-112">Area:</span></span>  <br/> |<span data-ttu-id="f2cc7-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="f2cc7-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2cc7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f2cc7-114">Remarks</span></span>

<span data-ttu-id="f2cc7-115">バイナリ文字列の内容は、メッセージの発信者によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="f2cc7-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="f2cc7-116">メッセージへの応答として生成されるすべてのレポートには、送信メッセージ、このプロパティのセットをコピーしてください。 場合、</span><span class="sxs-lookup"><span data-stu-id="f2cc7-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f2cc7-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f2cc7-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f2cc7-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f2cc7-118">Header files</span></span>

<span data-ttu-id="f2cc7-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2cc7-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2cc7-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2cc7-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2cc7-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f2cc7-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f2cc7-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f2cc7-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2cc7-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2cc7-123">See also</span></span>



[<span data-ttu-id="f2cc7-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2cc7-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2cc7-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2cc7-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2cc7-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f2cc7-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2cc7-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f2cc7-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

