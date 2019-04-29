---
title: 高度な検索の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407390"
---
# <a name="implementing-advanced-searching"></a>高度な検索の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳のコンテナーには、クライアントが**PR_DISPLAY_NAME**以外のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を検索できる高度な検索機能をサポートしているものがあります。 高度な検索をサポートするには、プロバイダーが他のコンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティを通じてアクセスできる特別なコンテナーを実装する必要があります。 **PR_SEARCH**には、高度な検索条件を入力および編集するために使用するダイアログボックスについて説明する表示テーブルへのアクセスを提供する container オブジェクトが含まれています。 
  
 **高度な検索をサポートするには**
  
1. 各検索基準のプロパティを定義します。
    
2. コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドの、 **PR_SEARCH**プロパティを処理するコードセクションで、次のように入力します。 
    
1. クライアントが**IMAPIContainer**インターフェイスを要求していることを確認します。 不適切なインターフェイスが要求されている場合は、エラーが発生し、MAPI_E_INTERFACE_NOT_SUPPORTED が返されます。 
    
2. **IMAPIContainer**インターフェイスをサポートする新しい検索オブジェクトを作成します。 
    
3. この時点で、検索コンテナーの**imapiprop:: openproperty**メソッドが**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを取得するための呼び出しが行われます。 プロバイダーでは、通常、コンテナーの [高度な検索] ダイアログボックスを記述する[builddisplaytable](builddisplaytable.md)を呼び出すことによって、表示テーブルを指定する必要があります。
    
4. MAPI [検索] ダイアログボックスを表示し、ユーザーが適切な条件を入力できるようにします。 ユーザーが完了すると、MAPI はコンテナーの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、検索条件を格納します。 
    
5. 検索コンテナーの contents テーブルを要求する呼び出しが行われます。 コンテンツテーブルに、条件に一致するコンテナー内のすべてのエントリを設定します。
    

