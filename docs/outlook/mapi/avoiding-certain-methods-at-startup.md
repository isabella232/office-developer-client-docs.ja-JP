---
title: 起動時に特定のメソッドを避けること。
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: db327fdd239684140e4feeeb2a6045a2fcd5c410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799741"
---
# <a name="avoiding-certain-methods-at-startup"></a>起動時に特定のメソッドを避けること。

 
  
**適用されます**: Outlook 
  
起動時にパフォーマンスを向上させるには、次の呼び出しを回避します。
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
**IMAPIStatus::ValidateState**への呼び出しでは、MAPI スプーラーを無効または MAPI のサブシステムのいずれかで行われるときにのみ、パフォーマンスに影響します。 これらのメソッドが起動処理を遅く理由は、MAPI スプーラーが、起動時のタスクを完了するまでに完了することはできませんのでです。 
  
起動時にメッセージ ・ ストアを検索しないようにします。 起動処理が終了したときに、 [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)の呼び出しを確認します。 
  

