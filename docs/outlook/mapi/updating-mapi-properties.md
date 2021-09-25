---
title: MAPI プロパティの更新
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 90af0f7226acbdbab4fde6480763d3415236cfcc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623972"
---
# <a name="updating-mapi-properties"></a>MAPI プロパティの更新

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントとサービス プロバイダーは、次の呼び出しによってプロパティ値を更新できます。
  
- オブジェクトの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを使用して、1 つ以上のオブジェクトのプロパティの値を更新します。 
    
- [HrSetOneProp](hrsetoneprop.md)関数は、一度に 1 つのプロパティのみを更新します。 ターゲット **オブジェクトがローカルの場合にのみ、HrSetOneProp** を使用します。この関数は、リモート オブジェクトで使用するとパフォーマンスが低下する可能性があります。 
    
次の手順は **、SetProps** を使用してメッセージ クラスまたはメッセージの PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを更新する方法を示しています。 
  
### <a name="to-update-the-message-class-of-a-message"></a>メッセージのメッセージ クラスを更新するには 
  
1. メッセージ クラス [に SPropValue](spropvalue.md) 構造体を割り当て、そのメンバーを適切に設定します。 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. メッセージの **IMAPIProp::SetProps** メソッドを呼び出して、新しいメッセージ クラスを設定します。 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)

