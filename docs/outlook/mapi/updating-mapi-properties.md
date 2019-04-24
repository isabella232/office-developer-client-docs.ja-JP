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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360516"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="59efa-103">MAPI プロパティの更新</span><span class="sxs-lookup"><span data-stu-id="59efa-103">Updating MAPI properties</span></span>

<span data-ttu-id="59efa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59efa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59efa-105">クライアントおよびサービスプロバイダーは、次のものを呼び出してプロパティの値を更新できます。</span><span class="sxs-lookup"><span data-stu-id="59efa-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="59efa-106">オブジェクトの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを実行して、1つ以上のオブジェクトのプロパティの値を更新します。</span><span class="sxs-lookup"><span data-stu-id="59efa-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="59efa-107">[hrsetoneprop](hrsetoneprop.md)関数は、一度に1つのプロパティのみを更新します。</span><span class="sxs-lookup"><span data-stu-id="59efa-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="59efa-108">**hrsetoneprop**は、対象のオブジェクトがローカルの場合にのみ使用します。この関数は、リモートオブジェクトと共に使用すると、パフォーマンスの低下を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="59efa-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="59efa-109">次の手順は、 **setprops**を使用してメッセージの message クラスまたは PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを更新する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="59efa-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="59efa-110">メッセージのメッセージクラスを更新するには</span><span class="sxs-lookup"><span data-stu-id="59efa-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="59efa-111">message クラスの[spropvalue](spropvalue.md)構造体を割り当て、そのメンバーを必要に応じて設定します。</span><span class="sxs-lookup"><span data-stu-id="59efa-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="59efa-112">メッセージの**imapiprop:: setprops**メソッドを呼び出して、新しいメッセージクラスを設定します。</span><span class="sxs-lookup"><span data-stu-id="59efa-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="59efa-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="59efa-113">See also</span></span>

- [<span data-ttu-id="59efa-114">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="59efa-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

