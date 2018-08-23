---
title: 配布リストのメンバーへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a32552343fa90dfbbb3571f50846976a5f5f5edd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595364"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>配布リストのメンバーへのアクセス

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 **配布リストのメンバーを取得するには**
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_DISPLAY_TYPE** ([など、取得するにはメンバーのプロパティを使用してサイズ プロパティ タグ配列を作成します。PidTagDisplayType](pidtagdisplaytype-canonical-property.md))。
    
2. 配布リストを開くには、[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。 
    
3. コンテンツ テーブルにアクセスするための配布リストの**IABContainer::GetContentsTable**メソッドを呼び出します。 
    
4. すべての配布リストのメンバーを表すテーブルの行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。 
    

