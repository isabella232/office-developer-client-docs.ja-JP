---
title: 配布リストのメンバーへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3a11b53aebf1e25ef93ac778da3e69401f1416f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605224"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>配布リストのメンバーへのアクセス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **配布リストのメンバーを取得するには**
  
1. PR_ENTRYID ([PidTagEntryId)](pidtagentryid-canonical-property.md) **、PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) **、PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)など、取得するメンバーのプロパティを含むサイズのプロパティ タグ **配列を** 作成します。
    
2. [IAddrBook::OpenEntry を呼び出して](iaddrbook-openentry.md)配布リストを開きます。 
    
3. 配布リストの **IABContainer::GetContentsTable** メソッドを呼び出して、そのコンテンツ テーブルにアクセスします。 
    
4. [HrQueryAllRows を](hrqueryallrows.md)呼び出して、配布リストのメンバーを表すテーブルのすべての行を取得します。 
    

