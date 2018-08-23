---
title: MAPI プロパティの更新
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804162"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="9d339-103">MAPI プロパティの更新</span><span class="sxs-lookup"><span data-stu-id="9d339-103">Updating MAPI properties</span></span>

<span data-ttu-id="9d339-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d339-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d339-105">クライアントとサービス ・ プロバイダーは、呼び出しによってプロパティの値を更新できます。</span><span class="sxs-lookup"><span data-stu-id="9d339-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="9d339-106">オブジェクトのプロパティの 1 つ以上の値を更新するオブジェクトの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="9d339-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="9d339-107">一度に 1 つのプロパティを更新するのには[HrSetOneProp](hrsetoneprop.md)関数です。</span><span class="sxs-lookup"><span data-stu-id="9d339-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="9d339-108">**HrSetOneProp**を使用して、対象のオブジェクトがローカルの場合のみこの関数は、リモート オブジェクトを使用すると、パフォーマンスの低下を発生できます。</span><span class="sxs-lookup"><span data-stu-id="9d339-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="9d339-109">**SetProps**を使用して、メッセージ クラス、またはメッセージの PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを更新する方法を次の手順に示します。</span><span class="sxs-lookup"><span data-stu-id="9d339-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="9d339-110">メッセージのメッセージ クラスを更新するには</span><span class="sxs-lookup"><span data-stu-id="9d339-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="9d339-111">メッセージ クラスの[SPropValue](spropvalue.md)構造体を割り当てるし、必要に応じてそのメンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="9d339-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="9d339-112">新しいメッセージ クラスを設定するのには、メッセージの**IMAPIProp::SetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9d339-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="9d339-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d339-113">See also</span></span>

- [<span data-ttu-id="9d339-114">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="9d339-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

