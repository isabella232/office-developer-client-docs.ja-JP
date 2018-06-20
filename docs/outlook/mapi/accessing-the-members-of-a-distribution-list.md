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
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799635"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>配布リストのメンバーへのアクセス

  
  
**適用されます**: Outlook 
  
 **配布リストのメンバーを取得するには**
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_DISPLAY_TYPE** ([など、取得するにはメンバーのプロパティを使用してサイズ プロパティ タグ配列を作成します。PidTagDisplayType](pidtagdisplaytype-canonical-property.md))。
    
2. 配布リストを開くには、[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。 
    
3. コンテンツ テーブルにアクセスするための配布リストの**IABContainer::GetContentsTable**メソッドを呼び出します。 
    
4. すべての配布リストのメンバーを表すテーブルの行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。 
    

