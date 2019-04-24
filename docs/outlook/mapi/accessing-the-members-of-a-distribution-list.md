---
title: 配布リストのメンバーへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331242"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>配布リストのメンバーへのアクセス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **配布リストのメンバーを取得するには**
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_DISPLAY_TYPE**など、取得するメンバーのプロパティを使用して、サイズが変更されたプロパティタグ配列を作成します ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
2. [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出して、配布リストを開きます。 
    
3. 配布リストの**IABContainer:: getcontentstable**メソッドを呼び出して、そのコンテンツテーブルにアクセスします。 
    
4. [hrqueryallrows](hrqueryallrows.md)を呼び出して、配布リストのメンバーを表すすべてのテーブルの行を取得します。 
    

