---
title: PidTagRecipientNumberForAdvice の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ac4da2d4082cac632548594411528b7bf1d6dc64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803277"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="f3374-103">PidTagRecipientNumberForAdvice の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f3374-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="f3374-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3374-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3374-105">このプロパティには、メッセージの受信者の連絡先電話番号メッセージの物理的な配信を通知するにはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f3374-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3374-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f3374-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3374-107">PR_RECIPIENT_NUMBER_FOR_ADVICE、PR_RECIPIENT_NUMBER_FOR_ADVICE_A、PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="f3374-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="f3374-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f3374-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3374-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="f3374-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="f3374-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f3374-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3374-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f3374-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f3374-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f3374-112">Area:</span></span>  <br/> |<span data-ttu-id="f3374-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="f3374-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3374-114">備考</span><span class="sxs-lookup"><span data-stu-id="f3374-114">Remarks</span></span>

<span data-ttu-id="f3374-115">これらのプロパティは、人間の受信者が配信時に予期しない電子メール ボックスではなく、物理的な宛先への配信と組み合わせて使用するものです。</span><span class="sxs-lookup"><span data-stu-id="f3374-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="f3374-116">例は、fax 送付状の電話番号です。</span><span class="sxs-lookup"><span data-stu-id="f3374-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f3374-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f3374-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f3374-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f3374-118">Header files</span></span>

<span data-ttu-id="f3374-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3374-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3374-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f3374-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3374-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3374-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f3374-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f3374-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3374-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3374-123">See also</span></span>



[<span data-ttu-id="f3374-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f3374-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3374-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f3374-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3374-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f3374-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3374-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f3374-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

