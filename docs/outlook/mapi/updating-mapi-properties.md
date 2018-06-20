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
# <a name="updating-mapi-properties"></a>MAPI プロパティの更新

**適用されます**: Outlook 
  
クライアントとサービス ・ プロバイダーは、呼び出しによってプロパティの値を更新できます。
  
- オブジェクトのプロパティの 1 つ以上の値を更新するオブジェクトの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドです。 
    
- 一度に 1 つのプロパティを更新するのには[HrSetOneProp](hrsetoneprop.md)関数です。 **HrSetOneProp**を使用して、対象のオブジェクトがローカルの場合のみこの関数は、リモート オブジェクトを使用すると、パフォーマンスの低下を発生できます。 
    
**SetProps**を使用して、メッセージ クラス、またはメッセージの PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを更新する方法を次の手順に示します。 
  
### <a name="to-update-the-message-class-of-a-message"></a>メッセージのメッセージ クラスを更新するには 
  
1. メッセージ クラスの[SPropValue](spropvalue.md)構造体を割り当てるし、必要に応じてそのメンバーを設定します。 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. 新しいメッセージ クラスを設定するのには、メッセージの**IMAPIProp::SetProps**メソッドを呼び出します。 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>関連項目

- [MAPI Property Overview](mapi-property-overview.md)

