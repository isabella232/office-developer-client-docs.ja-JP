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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438527"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="9ecb5-103">PidTagContentCorrelator 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ecb5-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="9ecb5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ecb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ecb5-105">メッセージの送信者が、元のメッセージとレポートを照合するために使用できる値を格納します。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ecb5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9ecb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ecb5-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="9ecb5-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="9ecb5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9ecb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ecb5-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="9ecb5-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="9ecb5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9ecb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ecb5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ecb5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ecb5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9ecb5-112">Area:</span></span>  <br/> |<span data-ttu-id="9ecb5-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="9ecb5-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ecb5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9ecb5-114">Remarks</span></span>

<span data-ttu-id="9ecb5-115">バイナリ文字列の内容は、メッセージの発信者によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="9ecb5-116">送信メッセージに設定されている場合、このプロパティはメッセージへの応答で生成されたすべてのレポートにコピーされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ecb5-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9ecb5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9ecb5-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9ecb5-118">Header files</span></span>

<span data-ttu-id="9ecb5-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ecb5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ecb5-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ecb5-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9ecb5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9ecb5-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ecb5-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ecb5-123">See also</span></span>



[<span data-ttu-id="9ecb5-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9ecb5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ecb5-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ecb5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ecb5-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9ecb5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ecb5-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9ecb5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

