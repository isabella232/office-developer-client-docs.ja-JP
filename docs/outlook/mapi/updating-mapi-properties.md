---
title: MAPI プロパティの更新
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407523"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="bd8fe-103">MAPI プロパティの更新</span><span class="sxs-lookup"><span data-stu-id="bd8fe-103">Updating MAPI properties</span></span>

<span data-ttu-id="bd8fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd8fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd8fe-105">クライアントとサービス プロバイダーは、次の呼び出しによってプロパティ値を更新できます。</span><span class="sxs-lookup"><span data-stu-id="bd8fe-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="bd8fe-106">オブジェクトの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを使用して、1 つ以上のオブジェクトのプロパティの値を更新します。</span><span class="sxs-lookup"><span data-stu-id="bd8fe-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="bd8fe-107">[HrSetOneProp](hrsetoneprop.md)関数は、一度に 1 つのプロパティのみを更新します。</span><span class="sxs-lookup"><span data-stu-id="bd8fe-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="bd8fe-108">ターゲット **オブジェクトがローカルの場合にのみ、HrSetOneProp** を使用します。この関数は、リモート オブジェクトで使用するとパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bd8fe-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="bd8fe-109">次の手順は **、SetProps** を使用してメッセージ クラスまたはメッセージの PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを更新する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bd8fe-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="bd8fe-110">メッセージのメッセージ クラスを更新するには</span><span class="sxs-lookup"><span data-stu-id="bd8fe-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="bd8fe-111">メッセージ クラス [に SPropValue](spropvalue.md) 構造体を割り当て、そのメンバーを適切に設定します。</span><span class="sxs-lookup"><span data-stu-id="bd8fe-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="bd8fe-112">メッセージの **IMAPIProp::SetProps** メソッドを呼び出して、新しいメッセージ クラスを設定します。</span><span class="sxs-lookup"><span data-stu-id="bd8fe-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="bd8fe-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd8fe-113">See also</span></span>

- [<span data-ttu-id="bd8fe-114">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="bd8fe-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

