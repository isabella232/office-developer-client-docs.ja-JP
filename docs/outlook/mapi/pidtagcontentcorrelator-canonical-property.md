---
title: PidTagContentCorrelator の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2290e6751778f17defc8d1007ff62c88f1b75465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802601"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="9ce2a-103">PidTagContentCorrelator の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9ce2a-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="9ce2a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ce2a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ce2a-105">元のメッセージを含むレポートを一致するようにメッセージの送信者を使用できる値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9ce2a-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ce2a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9ce2a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ce2a-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="9ce2a-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="9ce2a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9ce2a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ce2a-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="9ce2a-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="9ce2a-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9ce2a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ce2a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ce2a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ce2a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9ce2a-112">Area:</span></span>  <br/> |<span data-ttu-id="9ce2a-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="9ce2a-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ce2a-114">備考</span><span class="sxs-lookup"><span data-stu-id="9ce2a-114">Remarks</span></span>

<span data-ttu-id="9ce2a-115">バイナリ文字列の内容は、メッセージの発信者によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="9ce2a-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="9ce2a-116">メッセージへの応答として生成されるすべてのレポートには、送信メッセージ、このプロパティのセットをコピーしてください。 場合、</span><span class="sxs-lookup"><span data-stu-id="9ce2a-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ce2a-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9ce2a-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9ce2a-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9ce2a-118">Header files</span></span>

<span data-ttu-id="9ce2a-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ce2a-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ce2a-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9ce2a-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ce2a-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ce2a-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9ce2a-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9ce2a-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ce2a-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ce2a-123">See also</span></span>



[<span data-ttu-id="9ce2a-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ce2a-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ce2a-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ce2a-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ce2a-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9ce2a-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ce2a-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9ce2a-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

