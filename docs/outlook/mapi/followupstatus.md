---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568519"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージの別のフォロー アップのステータスを指定します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Members

 _flwupNone_
  
> フラグが指定されていません。
    
 _flwupComplete_
  
> メッセージは完了です。
    
 _flwupMarked_
  
> メッセージは、フラグを設定します。
    
 _flwupMAX_
  
> フォロー アップのためにサポートされている別の状態の数です。
    
## <a name="see-also"></a>関連項目



[PidTagFlagStatus 標準プロパティ](pidtagflagstatus-canonical-property.md)

