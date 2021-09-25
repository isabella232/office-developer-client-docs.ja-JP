---
title: '[高度な検索] ダイアログ ボックスの使用'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5498b6309c0c650f96503fbd30c62279c9dfd2ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578404"
---
# <a name="using-an-advanced-search-dialog-box"></a>[高度な検索] ダイアログ ボックスの使用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のアドレス帳コンテナーは高度な検索機能をサポートしています。これにより、クライアントは、ユーザー以外のプロパティ[(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)をPR_DISPLAY_NAME検索できます。 高度な検索をサポートするアドレス帳コンテナーには、PR_SEARCH ([PidTagSearch](pidtagsearch-canonical-property.md)) というコンテナー **オブジェクト プロパティ** があります。 このコンテナー オブジェクトは、検索ダイアログ ボックス (高度な検索条件の入力と編集に使用されるダイアログ ボックス) を説明する表示テーブルへのアクセスを提供します。
  
 **アドレス帳コンテナーで高度な検索を実行するには**
  
1. コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出し、プロパティ **タグ** PR_SEARCHインターフェイス識別子のIID_IMAPIContainerを指定します。 
    
2. プロパティ タグの PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) とインターフェイス識別子の **IID_IMAPITable** を指定して、検索オブジェクトの **IMAPIProp::OpenProperty** メソッドを呼び出します。 
    
3. 検索オブジェクトの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、高度な検索で使用するプロパティの値を確立します。 
    
4. 高度な検索条件を保存するには、検索オブジェクトの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出します。 
    
この一連の呼び出しは、クライアントが検索オブジェクトの **GetSearchCriteria** メソッドを呼び出す際に使用できる制限になります。 
  

