---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ad601ff547bfb89b98f0733b9e070b923ad92e1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556736"
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

