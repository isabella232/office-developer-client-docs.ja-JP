---
title: IAddrBook IMAPIProp
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 44bc6de420953bd665bd3caa336b76b15c1effd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579460"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI アドレス帳へのアクセスをサポートし、一般的なダイアログ ボックスを表示するなどの操作が含まれていますコンテナーでは、メッセージングのユーザー、および配布を開くの一覧が表示されます。名前解決を実行します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって公開されます。  <br/> |アドレス帳オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション、サービス ・ プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IAddrBook  <br/> |
|ポインターの型。  <br/> |LPADRBOOK  <br/> |
|トランザクション モデル:  <br/> |書き込み禁止  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |アドレス帳エントリを開き、エントリにアクセスするために使用するインターフェイスへのポインターを返します。  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |同じアドレス帳オブジェクトを参照しているかどうかを判断するのには、特定のアドレス帳プロバイダーに属している 2 つのエントリ id を比較します。  <br/> |
|[アドバイス](iaddrbook-advise.md) <br/> |アドレス帳の 1 つまたは複数のエントリへの変更に関する通知を受信するクライアントまたはサービス プロバイダーを登録します。  <br/> |
|[アドバイズ中止します。](iaddrbook-unadvise.md) <br/> |アドレス帳エントリを以前に確立された通知の登録をキャンセルします。  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |一時アドレスのエントリ id を作成します。  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |アドレス帳コンテナー、または送信メッセージの受信者の一覧には、新しい受信者を追加します。  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |宛先リスト内の受信者にエントリの識別子を割り当て、名前解決を実行します。  <br/> |
|[住所](iaddrbook-address.md) <br/> |Outlook アドレス帳] ダイアログ ボックスが表示されます。  <br/> |
|[詳細](iaddrbook-details.md) <br/> |特定のアドレス帳のエントリに関する詳細情報を表示するダイアログ ボックスが表示されます。  <br/> |
|**RecipOptions** <br/> | *いないサポートまたは文書化されています。*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *いないサポートまたは文書化されています。*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |個人用アドレス帳 (PAB) として指定されているコンテナーのエントリの識別子を返します。  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |個人用アドレス帳 (PAB) には、特定のコンテナーを指定します。  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |初期のアドレス帳コンテナーのエントリの識別子を返します。  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |既定のアドレス帳コンテナーとして最初に利用可能にするには、指定したコンテナーを確立します。  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |[ResolveName](iaddrbook-resolvename.md)メソッドによって開始された名前解決の処理に含まれるコンテナーのエントリ id の順序付きリストを返します。  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |名前解決の処理に使用されるプロファイルに新しい検索パスを設定します。  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |メッセージング システムによって後で使用できる受信者のリストを準備します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

