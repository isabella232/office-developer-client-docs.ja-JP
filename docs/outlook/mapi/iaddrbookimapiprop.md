---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2edbc66be1f2f2ae761677c425616e70b77096d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561552"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI アドレス帳へのアクセスをサポートし、一般的なダイアログ ボックスの表示などの操作が含まれます。コンテナー、メッセージング ユーザー、配布リストを開く。名前解決を実行します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|次のユーザーによって公開されます。  <br/> |アドレス帳オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション、サービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IAddrBook  <br/> |
|ポインターの種類:  <br/> |LPADRBOOK  <br/> |
|トランザクション モデル:  <br/> |書き込み不可  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |アドレス帳エントリを開き、エントリへのアクセスに使用できるインターフェイスへのポインターを返します。  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |特定のアドレス帳プロバイダーに属する 2 つのエントリ識別子を比較して、同じアドレス帳オブジェクトを参照するかどうかを判断します。  <br/> |
|[アドバイス](iaddrbook-advise.md) <br/> |アドレス帳内の 1 つ以上のエントリに対する変更に関する通知を受信するクライアントまたはサービス プロバイダーを登録します。  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |アドレス帳エントリに対して以前に確立された通知登録を取り消します。  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |1 回のアドレスのエントリ識別子を作成します。  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |アドレス帳コンテナーまたは送信メッセージの受信者リストに新しい受信者を追加します。  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |名前解決を実行し、受信者リストの受信者にエントリ識別子を割り当てる。  <br/> |
|[Address](iaddrbook-address.md) <br/> |[アドレスOutlook] ダイアログ ボックスを表示します。  <br/> |
|[詳細](iaddrbook-details.md) <br/> |特定のアドレス帳エントリに関する詳細を表示するダイアログ ボックスを表示します。  <br/> |
|**RecipOptions** <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |個人用アドレス帳 (PAB) として指定されているコンテナーのエントリ識別子を返します。  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |特定のコンテナーを個人用アドレス帳 (PAB) として指定します。  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |最初のアドレス帳コンテナーのエントリ識別子を返します。  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |指定したコンテナーを、最初に使用可能にした既定のアドレス帳コンテナーとして確立します。  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |ResolveName メソッドによって開始された名前解決プロセスに含めるコンテナーのエントリ識別子の順序付きリスト [を返](iaddrbook-resolvename.md) します。  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |名前解決プロセスに使用するプロファイル内の新しい検索パスを設定します。  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |メッセージング システムで後で使用する受信者リストを準備します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

