---
title: 起動時に特定のメソッドを回避
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '最終更新日: 2015 年 12 月 7 日'
ms.openlocfilehash: 345633700d921f617f65e0b5fefeba05deba7c72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605140"
---
# <a name="avoiding-certain-methods-at-startup"></a>起動時に特定のメソッドを回避

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
起動時のパフォーマンスを向上させるには、次の呼び出しを避けてください。
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
**IMAPIStatus::ValidateState** の呼び出しは、MAPI スプーラーまたは MAPI サブシステムのいずれかで行われた場合のみ、パフォーマンスに影響します。 これらのメソッドが起動処理を遅らせるのは、MAPI スプーラーが起動タスクを完了するまでそのメソッドが完了できないためです。 
  
また、起動時のメッセージ ストアの検索も避ける必要があります。 起動処理が終わってから、[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) の呼び出しを行ってください。 
  

