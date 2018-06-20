---
title: アドレス帳のエントリをコピーします。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ce7f7e2db341be62912935b7a55d69eaf5db8ab5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799828"
---
# <a name="copying-address-book-entries"></a>アドレス帳のエントリをコピーします。

  
  
**適用されます**: Outlook 
  
コンテナーの[IABContainer::CopyEntries](iabcontainer-copyentries.md)メソッドが呼び出されますから、同じ 1 つまたは複数の受信者このコンテナーにコピーするか、別のコンテナーです。 **CopyEntries**は、4 つの入力パラメーターを持つ: コピーする受信者を表すエントリの識別子、進行状況インジケーター、進行中のオブジェクト ポインター、およびフラグの値のウィンドウ ハンドルの配列。 プロバイダーは、AB_NO_DIALOG フラグが設定されていないと、オブジェクトを使用して、進行状況、 _lpProgress_パラメーターからが NULL でない場合、進行状況を表示する必要があります。 _LpProgress_が NULL の場合は、MAPI 処理中のオブジェクトを使用して[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)を呼び出します。 進行状況を表示する方法についての詳細については、[進行状況のインジケーターを表示する](mapi-progress-indicators.md)を参照してください。
  
以外に、進行状況インジケーターを非表示にする AB_NO_DIALOG は、他の 2 つのフラグの 1 つも設定型の重複するエントリのチェックを要求する: CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT です。 CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT のフラグは無視して、プロバイダーが重複したエントリを決定する方法についての提案のみです。 MAPI は、プロバイダーが次のようにこれらのフラグのサポートを実装することをお勧めします。
  
|**重複するエントリのフラグ**|**推奨される実装**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |コンテナー内のエントリの表示名を作成するエントリの表示名が一致したかどうかを確認してください。  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |表示名と検索キーの両方を作成するエントリのコンテナーのエントリの表示名と検索キーに一致するかどうかを確認してください。  <br/> |
   
最後のフラグでは、CREATE_REPLACE は、新しいエントリは、プロバイダーが作成されるエントリがコンテナー内のエントリの重複を決定する場合は既存の 1 つを置き換える必要がありますを示します。 
  
プロバイダーが個人用アドレス帳の場合は、コピー操作を行うたびに、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティが含まれます。 コピーの受信者の詳細表示のテーブルを含む、受信者ではなく呼び出し元のコンテナーに表示を作成するの詳細を表示するのには、コンテナーが有効にします。
  
 **IABContainer::CopyEntries を実装するには**
  
1. _LpEntries_パラメーターでは、各エントリ id は、プロバイダーを処理し、されていない場合は失敗し、MAPI_E_INVALID_ENTRYID を返す形式で、かどうかを決定します。 
    
2. 場合は、エントリ id は、メッセージングのユーザー、配布リスト、または、プロバイダーを処理するためのコンテナーを表します。
    
1. 開くには、対応する受信者の[IMAPISupport::OpenEntry](imapisupport-openentry.md)メソッドを呼び出します。 
    
2. 受信者コンテナーにコピーします。 
    
3. 場合はエントリの識別子は、外部の受信者を表しています。
    
1. 新しい受信者を作成するのには、コンテナーの[IABContainer::CreateEntry](iabcontainer-createentry.md)のメソッドを呼び出します。 
    
2. 新しい受信者には、初期のプロパティを設定します。
    
4. 保存するための新しいオブジェクトの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
5. 新しい受信者を反映するためにコンテナーの内容のテーブルを更新します。 
    
6. 登録済みクライアントにテーブルの通知を送信する[IMAPISupport::Notify](imapisupport-notify.md)を呼び出します。 
    

