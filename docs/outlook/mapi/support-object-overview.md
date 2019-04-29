---
title: サポートオブジェクトの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 55d8a9c78ae5132eaa8cf0f0aec5b252ef83b926
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433613"
---
# <a name="support-object-overview"></a>サポートオブジェクトの概要

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI furnishes は、すべてのサービスプロバイダー用の[imapisupport: IUnknown](imapisupportiunknown.md)インターフェイスを実装するオブジェクトで、構成中にすべてのメッセージサービスに対して使用されます。 
  
サポートオブジェクトはクライアントからアクセスできません。これらは MAPI によって実装され、サービスプロバイダーによってのみ呼び出されます。 **imapisupport**インターフェイスは、Mapispi ヘッダーファイルで指定されています。 その識別子は IID_IMAPISup で、ポインターの種類は LPMAPISUP です。 サポートオブジェクトによって、MAPI プロパティは公開されません。 
  
プロバイダーには、1つまたは複数のサポートオブジェクトを指定できます。これは、MAPI がプロバイダーをログに記録した回数またはプロバイダーのメッセージサービスの entry 関数が呼び出された回数によって決まります。 通常、プロバイダーは、セッションごとに少なくとも1回はログインします。 クライアントがセッションを要求するプロファイルエントリを使用してセッションを開始するたびに、アドレス帳とトランスポートプロバイダーがログオンします。 クライアントが[imapisession:: openmsgstore](imapisession-openmsgstore.md)メソッドを呼び出すたびに、メッセージストアプロバイダーがログインします。 
  
セッションで複数のログオンがある場合は、1つのサポートオブジェクトを保持して使用するか、個別に使用するか、または、その後のサポートオブジェクトを破棄するかを選択できます。 サポートオブジェクトを保持するには、 **IUnknown:: AddRef**メソッドを呼び出します。 セッション全体を保持する必要があるサポートオブジェクトに対して**AddRef**を呼び出すことは非常に重要です。呼び出しが行われていない場合、MAPI はサポートオブジェクトを解放し、そのメモリを解放します。 
  
サポートオブジェクトの目的は、プロバイダーが一般的に使用する多くのメソッドの実装を提供することです。 各サポートオブジェクトには、プロバイダーが実行されているセッション、プロバイダーが使用しているプロファイルセクション、セッションのエラー情報など、独自のインスタンスに固有のコンテキストデータも含まれています。 
  
サポートオブジェクトには、主なプロバイダーの種類 (アドレス帳、メッセージストア、トランスポート) ごとに1つと構成サポート用の4つの種類があります。 
  
MAPI では、その使用に関連するメソッドの実装を含めることによって、各サポートオブジェクトをカスタマイズします。 [imapisupport:: openプロファイル](imapisupport-openprofilesection.md)のようないくつかのメソッドの実装は、すべてのサポートオブジェクトに含まれています。 [imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)などの他のメソッドの実装は、特定のサポートオブジェクトにのみ適用されます。 このメソッドを使用できるのは、メッセージストアとトランスポートプロバイダーのみです。アドレス帳プロバイダーまたはメッセージサービスが呼び出しを試みると、MAPI は MAPI_E_NO_SUPPORT を返します。
  
サポートオブジェクトは、次のような多くのタスクを実行するために使用できます。
  
- プロファイルセクションへのアクセス。
    
- フォルダーまたはメッセージをコピーする。 詳細については、「[メッセージまたはフォルダーをコピーまたは移動する](copying-or-moving-a-message-or-a-folder.md)」を参照してください。
    
- 他のプロバイダーに属するオブジェクトへのアクセス。 詳細については、「[オブジェクトのアクセスと比較のサポート](supporting-object-access-and-comparison.md)」を参照してください。 
    
- イベント通知の処理。 詳細については、「[イベント通知のサポート](supporting-event-notification.md)」を参照してください。
    
- メモリの割り当てと解放。
    
- 一意の識別子を取得します。
    
- オブジェクトを無効にする。
    
- エラーを処理する。
    
- メッセージ preprocessors を登録します。 
    
- メッセージ配信レポートの準備。 
    
ログオン時に、MAPI は各サービスプロバイダーのプロバイダーオブジェクトの logon メソッドを呼び出します。 アドレス帳プロバイダーの場合、MAPI は[IABProvider:: Logon](iabprovider-logon.md)を呼び出します。 メッセージストアプロバイダーの場合、MAPI は[IMSProvider:: Logon](imsprovider-logon.md)を呼び出します。 トランスポートプロバイダーの場合、MAPI は[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)を呼び出します。 MAPI は、このメソッドへのパラメーターのいずれかで、適切なサポートオブジェクトへのポインターを渡します。 ログオン方法では、ログオンオブジェクトをインスタンス化し、サポートオブジェクトポインターを渡します。 logon オブジェクトは、必要に応じて、サポートオブジェクトの**IUnknown:: AddRef**メソッドを呼び出して保持します。 サービスプロバイダーのログオンプロセスの詳細については、「[サービスプロバイダーを開始する](starting-a-service-provider.md)」を参照してください。
  
クライアントがログオフすると、MAPI はログオンオブジェクトの logoff メソッドを呼び出します。 logoff メソッドは、サポートオブジェクトの**IUnknown:: Release**メソッドを呼び出して、プロバイダーがサポート方法を呼び出すことがなくなったことを示します。 ログオンの場合と同様に、logoff メソッドの名前は少し異なります。 [IABLogon](iablogoniunknown.md)および[IMSLogon](imslogoniunknown.md)インターフェイスには、 **Logoff**メソッドがあります。[IXPLogon](ixplogoniunknown.md)インターフェイスには、 [transportlogoff](ixplogon-transportlogoff.md)メソッドがあります。 
  
メッセージサービスエントリポイント関数は、ログオン試行がエラー MAPI_E_UNCONFIGURED で失敗したとき、またはクライアントが構成要求を開始したときに呼び出されます。 MAPI は、構成のサポートオブジェクトをインスタンス化し、構成が変更されることがないプロバイダーまたはプロバイダーのいずれかに対して、メッセージサービスエントリポイント関数を呼び出します。 その他のサポートオブジェクトとは異なり、構成サポートオブジェクトは、エントリポイント関数が戻るまで有効です。メッセージサービスは、これらのオブジェクトの**AddRef**メソッドを呼び出して保持しません。 
  
通常、MAPI はプロバイダーのメッセージサービスのエントリポイント関数に対して呼び出しを行いますが、プロバイダーから呼び出しを要求される場合もあります。 これは、クライアントがプロバイダーの[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドを呼び出して、プロバイダーに構成プロパティシートを表示するように求める場合に、発生する可能性があります。 **settingsdialog**は、メッセージサービスエントリポイント関数に渡すことができる構成サポートオブジェクトを取得するために、 [imapisupport:: GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md)を呼び出す必要があります。 
  
[imapisupport:: getmemallocroutines](imapisupport-getmemallocroutines.md)メソッドを使用して、MAPI でリンクしなくてもメモリの割り当てと解放関数のアドレスを判別できます。 **getmemallocroutines**を使用すると、デバッグコードを使用して割り当て関数の呼び出しを囲むことにより、メモリリークのトレースが容易になります。 推奨されているように**getmemallocroutines**を呼び出す場合は、 [createiprop](createiprop.md)関数を呼び出す前に実行してください。これには、アロケーション関数のアドレスをパラメーターとして指定する必要があります。 
  
新しいアドレス帳またはメッセージストアオブジェクトを作成する必要がある場合は、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティでオブジェクトの検索キーを作成して設定します。 検索キーを作成するために使用する一意の識別子を取得するには、 [「imapisupport:: newuid](imapisupport-newuid.md) 」を呼び出します。 独自のハードコーディングされた[MAPIUID](mapiuid.md)は使用しないでください。 プロバイダーの**MAPIUID**は、エントリ識別子に対してのみ使用する必要があります。 検索キーの作成方法の詳細については、「 [MAPI レコードおよび検索キー](mapi-record-and-search-keys.md)」を参照してください。
  
クライアントアプリケーションは、1つ以上の関連オブジェクトを解放せずにオブジェクトを解放する場合があります。 このような場合、プロバイダーは解放されていないオブジェクトを使用できないようにする必要があります。 これを行うために、プロバイダーは、オブジェクトに接続されているすべてのリソースを解放し、 [imapisupport:: makeinvalid](imapisupport-makeinvalid.md)を呼び出して、オブジェクトの vtable を無効にします。 **makeinvalid**は、vtable の**IUnknown**メソッド (**QueryInterface**、 **AddRef**、および**Release**) を標準の MAPI 実装に置き換え、他のすべてのメソッドが MAPI_E_INVALID_OBJECT を返すようにします。 **makeinvalid**は、vtable 以外のすべてのオブジェクトのメモリも解放します。 
  
## <a name="see-also"></a>関連項目



[MAPI サービスプロバイダー](mapi-service-providers.md)

