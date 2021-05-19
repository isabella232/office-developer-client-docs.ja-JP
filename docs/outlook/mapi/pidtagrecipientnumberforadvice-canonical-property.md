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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420641"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="70287-103">PidTagRecipientNumberForAdvice 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="70287-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="70287-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70287-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70287-105">このプロパティには、メッセージの物理的な配信を通知するために呼び出すメッセージ受信者の電話番号が含まれる。</span><span class="sxs-lookup"><span data-stu-id="70287-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70287-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="70287-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70287-107">PR_RECIPIENT_NUMBER_FOR_ADVICE、PR_RECIPIENT_NUMBER_FOR_ADVICE_A、PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="70287-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="70287-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="70287-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70287-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="70287-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="70287-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="70287-110">Data type:</span></span>  <br/> |<span data-ttu-id="70287-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70287-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="70287-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="70287-112">Area:</span></span>  <br/> |<span data-ttu-id="70287-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="70287-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70287-114">注釈</span><span class="sxs-lookup"><span data-stu-id="70287-114">Remarks</span></span>

<span data-ttu-id="70287-115">これらのプロパティは、人間の受信者が配信時に存在すると予想されない場合に、電子メールボックスではなく、物理的な宛先への配信と組み合わせて使用することを目的とします。</span><span class="sxs-lookup"><span data-stu-id="70287-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="70287-116">たとえば、FAX カバー シートの電話番号です。</span><span class="sxs-lookup"><span data-stu-id="70287-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="70287-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="70287-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="70287-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="70287-118">Header files</span></span>

<span data-ttu-id="70287-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70287-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="70287-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="70287-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="70287-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="70287-121">Mapitags.h</span></span>
  
> <span data-ttu-id="70287-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="70287-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70287-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="70287-123">See also</span></span>



[<span data-ttu-id="70287-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="70287-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70287-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="70287-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70287-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="70287-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70287-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="70287-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

