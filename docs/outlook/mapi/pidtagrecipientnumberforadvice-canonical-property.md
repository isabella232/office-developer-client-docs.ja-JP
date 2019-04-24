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
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356694"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="44341-103">PidTagRecipientNumberForAdvice 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44341-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="44341-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44341-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44341-105">このプロパティには、メッセージの物理的な配信をアドバイスするために呼び出すメッセージ受信者の電話番号が含まれます。</span><span class="sxs-lookup"><span data-stu-id="44341-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44341-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="44341-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44341-107">PR_RECIPIENT_NUMBER_FOR_ADVICE、PR_RECIPIENT_NUMBER_FOR_ADVICE_A、PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="44341-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="44341-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="44341-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44341-109">0x0c14</span><span class="sxs-lookup"><span data-stu-id="44341-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="44341-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="44341-110">Data type:</span></span>  <br/> |<span data-ttu-id="44341-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="44341-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="44341-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="44341-112">Area:</span></span>  <br/> |<span data-ttu-id="44341-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="44341-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44341-114">解説</span><span class="sxs-lookup"><span data-stu-id="44341-114">Remarks</span></span>

<span data-ttu-id="44341-115">これらのプロパティは、電子メールボックスではなく、物理的な送信先への配信と組み合わせて使用することを目的としていますが、配信時に人間の受信者が存在しないことが想定されているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="44341-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="44341-116">この例は、fax 送付状の電話番号です。</span><span class="sxs-lookup"><span data-stu-id="44341-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44341-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="44341-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="44341-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="44341-118">Header files</span></span>

<span data-ttu-id="44341-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44341-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="44341-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="44341-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="44341-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="44341-121">Mapitags.h</span></span>
  
> <span data-ttu-id="44341-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="44341-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44341-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="44341-123">See also</span></span>



[<span data-ttu-id="44341-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="44341-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44341-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44341-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44341-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="44341-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44341-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="44341-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

