---
title: '[高度な検索] ダイアログ ボックスの使用'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 581607e184d67413e735c4cbfb874643b3222a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588770"
---
# <a name="using-an-advanced-search-dialog-box"></a>[高度な検索] ダイアログ ボックスの使用

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
いくつかのアドレス帳コンテナーは、クライアントの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 以外のプロパティで検索できるようにする、高度な検索機能をサポートします。 高度な検索をサポートしているアドレス帳コンテナーには、 **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) と呼ばれるコンテナー オブジェクト プロパティが設定されています。 このコンテナー オブジェクトは、[検索] ダイアログ ボックスを説明する表示のテーブルへのアクセスを提供: ダイアログ ボックスを入力し、高度な検索条件を編集するために使用します。
  
 **アドレス帳コンテナーの高度な検索を実行するには**
  
1. インターフェイス識別子のプロパティ タグと IID_IMAPIContainer の**PR_SEARCH**を指定するコンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 
    
2. インターフェイス識別子のプロパティ タグと IID_IMAPITable の**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) を指定する、検索オブジェクトの**IMAPIProp::OpenProperty**メソッドを呼び出します。 
    
3. 高度な検索で使用するプロパティの値を確立するための検索オブジェクトの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。 
    
4. 高度な検索条件を保存するのには、検索オブジェクトの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
この一連の呼び出しは、クライアントが検索オブジェクトの**GetSearchCriteria**メソッドを呼び出すときに使用される制限の中で発生します。 
  

