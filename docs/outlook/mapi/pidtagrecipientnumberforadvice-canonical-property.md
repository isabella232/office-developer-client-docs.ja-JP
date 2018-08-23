---
title: PidTagRecipientNumberForAdvice 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3f23a332ee6778f71ce0809dfae8c0b6a92246a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595147"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="a4f7f-103">PidTagRecipientNumberForAdvice 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a4f7f-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="a4f7f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4f7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4f7f-105">このプロパティには、メッセージの受信者の連絡先電話番号メッセージの物理的な配信を通知するにはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a4f7f-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4f7f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4f7f-107">PR_RECIPIENT_NUMBER_FOR_ADVICE、PR_RECIPIENT_NUMBER_FOR_ADVICE_A、PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="a4f7f-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="a4f7f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4f7f-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="a4f7f-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="a4f7f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a4f7f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4f7f-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a4f7f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a4f7f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-112">Area:</span></span>  <br/> |<span data-ttu-id="a4f7f-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="a4f7f-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4f7f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a4f7f-114">Remarks</span></span>

<span data-ttu-id="a4f7f-115">これらのプロパティは、人間の受信者が配信時に予期しない電子メール ボックスではなく、物理的な宛先への配信と組み合わせて使用するものです。</span><span class="sxs-lookup"><span data-stu-id="a4f7f-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="a4f7f-116">例は、fax 送付状の電話番号です。</span><span class="sxs-lookup"><span data-stu-id="a4f7f-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a4f7f-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a4f7f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a4f7f-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a4f7f-118">Header files</span></span>

<span data-ttu-id="a4f7f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4f7f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4f7f-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a4f7f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4f7f-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4f7f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a4f7f-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a4f7f-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4f7f-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4f7f-123">See also</span></span>



[<span data-ttu-id="a4f7f-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a4f7f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4f7f-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a4f7f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4f7f-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a4f7f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4f7f-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a4f7f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

