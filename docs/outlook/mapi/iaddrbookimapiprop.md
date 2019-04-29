---
title: IAddrBook imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429825"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI アドレス帳へのアクセスをサポートし、コモンダイアログボックスを表示するなどの操作を含みます。コンテナー、メッセージングユーザー、および配布リストを開きます。名前解決を実行する。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|公開者:  <br/> |アドレス帳オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーション、サービスプロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IAddrBook  <br/> |
|ポインターの種類:  <br/> |lpadrbook  <br/> |
|トランザクションモデル:  <br/> |書き込み不可  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |アドレス帳エントリを開き、エントリへのアクセスに使用できるインターフェイスへのポインターを返します。  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |特定のアドレス帳プロバイダーに属する2つのエントリ識別子を比較して、同じアドレス帳オブジェクトを参照しているかどうかを判断します。  <br/> |
|[助言](iaddrbook-advise.md) <br/> |クライアントまたはサービスプロバイダーに、アドレス帳の1つまたは複数のエントリの変更に関する通知を受信するように登録します。  <br/> |
|[アドバイズ](iaddrbook-unadvise.md) <br/> |以前にアドレス帳エントリに対して設定された通知登録を取り消します。  <br/> |
|[createoneoff](iaddrbook-createoneoff.md) <br/> |1回限りのアドレスのエントリ id を作成します。  <br/> |
|[newentry](iaddrbook-newentry.md) <br/> |新しい受信者をアドレス帳コンテナーまたは送信メッセージの受信者リストに追加します。  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |名前解決を実行し、受信者リスト内の受信者にエントリ識別子を割り当てます。  <br/> |
|[住所](iaddrbook-address.md) <br/> |[Outlook アドレス帳] ダイアログボックスを表示します。  <br/> |
|[詳細](iaddrbook-details.md) <br/> |特定のアドレス帳エントリの詳細を表示するダイアログボックスを表示します。  <br/> |
|**RecipOptions** <br/> | *サポートされていないか文書化されていません。*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *サポートされていないか文書化されていません。*  <br/> |
|[getpab](iaddrbook-getpab.md) <br/> |個人用アドレス帳 (PAB) として指定されているコンテナーのエントリ識別子を返します。  <br/> |
|[setpab](iaddrbook-setpab.md) <br/> |特定のコンテナーを個人用アドレス帳 (PAB) として指定します。  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |最初のアドレス帳コンテナーのエントリ識別子を返します。  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |指定したコンテナーを、最初に使用可能にする既定のアドレス帳コンテナーとして確立します。  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |[ResolveName](iaddrbook-resolvename.md)メソッドによって開始された名前解決プロセスに含まれるコンテナーのエントリ id の順序付きリストを返します。  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |名前解決プロセスで使用されるプロファイルに新しい検索パスを設定します。  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |メッセージングシステムで後で使用するために、受信者リストを準備します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

