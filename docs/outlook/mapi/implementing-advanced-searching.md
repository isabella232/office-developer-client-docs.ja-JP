---
title: 高度な検索の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 20282c78f6ff9003221429046fa9126cc4abaeec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610469"
---
# <a name="implementing-advanced-searching"></a>高度な検索の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のアドレス帳コンテナーは高度な検索機能をサポートしています。これにより、クライアントは、ユーザー以外のプロパティ[(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)をPR_DISPLAY_NAME検索できます。 高度な検索をサポートするには、プロバイダーは、他のコンテナーの **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティからアクセスできる特別なコンテナーを実装する必要があります。 **PR_SEARCH** には、高度な検索条件の入力および編集に使用されるダイアログ ボックスを説明する表示テーブルへのアクセスを提供するコンテナー オブジェクトが含まれます。 
  
 **高度な検索をサポートするために**
  
1. 検索条件ごとにプロパティを定義します。
    
2. コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドのコードのセクションで、次のプロパティを **PR_SEARCH** します。 
    
1. クライアントが **IMAPIContainer インターフェイスを要求しているのを確認** します。 不適切なインターフェイスが要求されている場合は、エラーが発生し、MAPI_E_INTERFACE_NOT_SUPPORTED。 
    
2. IMAPIContainer インターフェイスをサポートする新 **しい検索オブジェクトを作成** します。 
    
3. この時点で、検索コンテナーの **IMAPIProp::OpenProperty** メソッドを呼び出して、その PR_DETAILS_TABLE **(** [PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを取得します。 プロバイダーは、通常、コンテナーの高度な検索ダイアログ ボックスを記述する [BuildDisplayTable](builddisplaytable.md)の呼び出しを通じて表示テーブルを提供する必要があります。
    
4. MAPI は、ユーザーが適切な条件を入力できるように、検索ダイアログ ボックスを表示します。 ユーザーが終了すると、MAPI はコンテナーの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して検索条件を格納します。 
    
5. 検索コンテナーのコンテンツ テーブルを要求する呼び出しが行されます。 コンテンツ テーブルに、条件に一致するコンテナー内のすべてのエントリを設定します。
    

