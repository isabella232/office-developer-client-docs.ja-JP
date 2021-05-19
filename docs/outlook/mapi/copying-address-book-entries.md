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
  
コンテナーの [IABContainer::CopyEntries](iabcontainer-copyentries.md) メソッドは、同じコンテナーまたは別のコンテナーから 1 つ以上の受信者をこのコンテナーにコピーするときに呼び出されます。 **CopyEntries** には、コピーする受信者を表すエントリ識別子の配列、進行状況インジケーターのウィンドウ ハンドル、進行状況オブジェクト ポインター、フラグ値の 4 つの入力パラメーターがあります。 プロバイダーは、AB_NO_DIALOG フラグが設定されていない場合は進行状況を表示し、null 以外の場合は  _lpProgress_ パラメーターの progress オブジェクトを使用する必要があります。 _lpProgress が_ NULL の場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)を呼び出して MAPI 進行状況オブジェクトを使用します。 進行状況の表示の詳細については、「進行状況インジケーターの [表示」を参照してください](mapi-progress-indicators.md)。
  
進行状況インジケーターをAB_NO_DIALOGに加えて、他の 2 つのフラグの 1 つを設定して、重複するエントリチェックの種類 (CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT) を要求できます。 このCREATE_CHECK_DUP_LOOSEフラグCREATE_CHECK_DUP_STRICTは、プロバイダーが重複するエントリを決定する方法についてのみ提案され、無視できます。 MAPI は、プロバイダーが次のようにこれらのフラグのサポートを実装するように提案します。
  
|**重複するエントリ フラグ**|**推奨される実装**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |作成するエントリの表示名が、コンテナー内の既にエントリの表示名と一致していないか確認します。  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |作成するエントリの表示名と検索キーの両方が、コンテナー エントリの表示名と検索キーと一致しないか確認します。  <br/> |
   
最後のフラグ CREATE_REPLACE は、プロバイダーが作成するエントリがコンテナー内の既にエントリと重複すると判断した場合、新しいエントリが既存のエントリを置き換える必要があります。 
  
プロバイダーが個人用アドレス帳の場合は、すべてのコピー **操作** に PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを含める必要があります。 コピーされた受信者の詳細表示テーブルを含め、元のコンテナーを呼び出して表示を作成するのではなく、コンテナーで受信者の詳細を表示できます。
  
 **IABContainer を実装するには::CopyEntries**
  
1. _lpEntries_ パラメーター内の各エントリ識別子が、プロバイダーが処理する形式かどうかを確認し、処理しない場合は失敗し、MAPI_E_INVALID_ENTRYID。 
    
2. エントリ識別子が、プロバイダーが処理するメッセージング ユーザー、配布リスト、またはコンテナーを表す場合は、次の操作を行います。
    
1. [IMAPISupport::OpenEntry](imapisupport-openentry.md)メソッドを呼び出して、対応する受信者を開きます。 
    
2. 受信者をコンテナーにコピーします。 
    
3. エントリ識別子が外部受信者を表す場合:
    
1. コンテナーの [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドを呼び出して、新しい受信者を作成します。 
    
2. 新しい受信者に初期プロパティを設定します。
    
4. 新しいオブジェクトの [IMAPIProp::SaveChanges メソッドを呼](imapiprop-savechanges.md) び出して保存します。 
    
5. コンテナーのコンテンツ テーブルを更新して、新しい受信者を反映します。 
    
6. [IMAPISupport::Notify](imapisupport-notify.md)を呼び出して、登録済みのクライアントにテーブル通知を送信します。 
    

