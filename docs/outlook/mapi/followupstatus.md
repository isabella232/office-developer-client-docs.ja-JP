---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418331"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの別のフォローアップ状態を指定します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>メンバー

 _flwupNone_
  
> フォローアップが指定されていません。
    
 _flwupComplete_
  
> メッセージが完了しました。
    
 _flwupMarked_
  
> メッセージにはフォローアップのマークが付きます。
    
 _flwupMAX_
  
> フォローアップでサポートされるさまざまな状態の数。
    
## <a name="see-also"></a>関連項目



[PidTagFlagStatus 標準プロパティ](pidtagflagstatus-canonical-property.md)

