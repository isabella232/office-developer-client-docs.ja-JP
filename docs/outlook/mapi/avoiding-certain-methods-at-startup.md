---
title: 起動時に特定のメソッドを回避
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '最終更新日: 2015 年 12 月 7 日'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580636"
---
# <a name="avoiding-certain-methods-at-startup"></a>起動時に特定のメソッドを回避

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
起動時のパフォーマンスを向上させるには、次の呼び出しを避けてください。
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
**IMAPIStatus::ValidateState**の呼び出しは、 MAPI スプーラーまたは MAPI サブシステムのいずれかで行われた場合のみ、パフォーマンスに影響します。 これらのメソッドが起動処理を遅らせるのは、MAPI スプーラーが起動タスクを完了するまでこれらのメソッドが完了できないためです。 
  
また、起動時のメッセージ ストアの検索も避ける必要があります。 起動処理が終わってから、 [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)の呼び出しを行ってください。 
  

