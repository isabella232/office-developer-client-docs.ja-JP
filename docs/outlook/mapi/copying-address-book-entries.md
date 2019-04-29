---
title: アドレス帳エントリのコピー
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418744"
---
# <a name="copying-address-book-entries"></a>アドレス帳エントリのコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同じまたは別のコンテナーの1人または複数の受信者がこのコンテナーにコピーされると、コンテナーの[IABContainer:: copyentries](iabcontainer-copyentries.md)メソッドが呼び出されます。 **copyentries**には4つの入力パラメーターがあります。コピーされる受信者を表すエントリ識別子の配列、進行状況インジケーターのウィンドウハンドル、進行状況オブジェクトポインター、およびフラグ値があります。 AB_NO_DIALOG フラグが設定されていない場合はプロバイダーに進行状況が表示され、NULL でない場合は_lpprogress_パラメーターから progress オブジェクトを使用する必要があります。 _lpprogress_が NULL の場合は、MAPI progress オブジェクトを使用するために、 [imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)を呼び出します。 進捗状況の表示の詳細については、「[進行状況インジケーターの表示](mapi-progress-indicators.md)」を参照してください。
  
進行状況インジケーターを表示しないように AB_NO_DIALOG に加えて、他の2つのフラグのいずれかを設定して、重複するエントリチェックの種類を要求することができます: CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT。 CREATE_CHECK_DUP_LOOSE および CREATE_CHECK_DUP_STRICT フラグは、プロバイダーが重複エントリを決定し、無視できるようにするための推奨事項に過ぎません。 MAPI では、次のように、これらのフラグのサポートを実装することをお勧めします。
  
|**重複するエントリフラグ**|**推奨される実装**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |作成するエントリの表示名が、コンテナー内に既にあるエントリの表示名と一致しているかどうかを確認します。  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |作成するエントリの表示名と検索キーの両方が、コンテナーエントリの表示名と検索キーと一致するかどうかを確認します。  <br/> |
   
最後のフラグ CREATE_REPLACE は、作成するエントリがコンテナー内に既に存在するエントリと重複しているとプロバイダーが判断した場合に、新しいエントリが既存のエントリを置き換える必要があることを示します。 
  
プロバイダーが個人用アドレス帳の場合は、すべてのコピー操作に**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを含めます。 コピーされた受信者の詳細表示テーブルを含めると、表示を作成する元のコンテナーを呼び出すことなく、受信者の詳細をコンテナーで表示できるようになります。
  
 **IABContainer:: copyentries を実装するには**
  
1. _lpentries_パラメーターの各エントリ識別子が、プロバイダーが処理し、失敗した場合は、MAPI_E_INVALID_ENTRYID を返すかどうかを決定します。 
    
2. エントリ識別子が、プロバイダーが処理するメッセージングユーザー、配布リスト、またはコンテナーを表している場合は、次のようになります。
    
1. [imapisupport:: openentry](imapisupport-openentry.md)メソッドを呼び出して、対応する受信者を開きます。 
    
2. 受信者をコンテナーにコピーします。 
    
3. エントリ識別子が外部の受信者を表す場合:
    
1. コンテナーの[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを呼び出して、新しい受信者を作成します。 
    
2. 新しい受信者の初期プロパティを設定します。
    
4. 新しいオブジェクトの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して保存します。 
    
5. コンテナーの contents テーブルを更新して、新しい受信者を反映させます。 
    
6. Call [imapisupport::](imapisupport-notify.md)登録済みクライアントにテーブル通知を送信するよう通知します。 
    

