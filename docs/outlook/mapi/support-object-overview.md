---
title: サポート オブジェクトの概要
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
# <a name="support-object-overview"></a>サポート オブジェクトの概要

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は [、IMAPISupport : IUnknown](imapisupportiunknown.md) インターフェイスを実装するオブジェクトであるサポート オブジェクトを、ログオン中のすべてのサービス プロバイダーと構成中のすべてのメッセージ サービスに提供します。 
  
サポート オブジェクトはクライアントからアクセスできない。MAPI によって実装され、サービス プロバイダーによってのみ呼び出されます。 **IMAPISupport インターフェイス** は Mapispi.h ヘッダー ファイルで指定されます。 その識別子はIID_IMAPISup、ポインターの種類は LPMAPISUP です。 MAPI プロパティはサポート オブジェクトによって公開されません。 
  
プロバイダーには、MAPI がプロバイダーをログオンする回数、またはプロバイダーのメッセージ サービス エントリ関数が呼び出された回数に応じて、1 つ以上のサポート オブジェクトを指定できます。 通常、プロバイダーはセッションごとに少なくとも 1 回ログオンします。 アドレス帳とトランスポート プロバイダーは、クライアントが要求するプロファイル エントリでセッションを開始する度にログオンします。 メッセージ ストア プロバイダーは、クライアントが [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを呼び出す度にログオンします。 
  
セッション内の複数のログオンの場合は、各サポート オブジェクトを個別に保持して使用するか、1 つ目のサポート オブジェクトのみを保持して使用するかのどちらかを選択し、後続の各サポート オブジェクトを破棄します。 サポート オブジェクトを保持するには、 **その IUnknown::AddRef メソッドを呼び出** します。 セッション **全体で保持** するサポート オブジェクトで AddRef を呼び出すのは非常に重要です。呼び出しが行われた場合、MAPI はサポート オブジェクトを解放し、そのメモリを解放します。 
  
サポート オブジェクトの目的は、プロバイダーが一般的に使用するメソッドの数がかなり多い場合に実装を提供します。 各サポート オブジェクトには、プロバイダーが実行しているセッション、プロバイダーが使用しているプロファイル セクション、セッションのエラー情報など、独自のインスタンスに固有のコンテキスト データも含まれる。 
  
サポート オブジェクトには、主要なプロバイダーの種類 (アドレス帳、メッセージ ストア、トランスポート) ごとに 1 つ、構成サポート用の 4 種類があります。 
  
MAPI では、使用に関連するメソッドの実装を含めて、各サポート オブジェクトをカスタマイズします。 [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)などの一部のメソッドの実装は、すべてのサポート オブジェクトに含まれています。 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)などの他のメソッドの実装は、特定のサポート オブジェクトにのみ適用されます。 このメソッドを使用できるのは、メッセージ ストアとトランスポート プロバイダーのみです。アドレス帳プロバイダーまたはメッセージ サービスが呼び出しを試みた場合、MAPI はアドレス帳プロバイダーをMAPI_E_NO_SUPPORT。
  
サポート オブジェクトは、次のような多くのタスクを実行するために使用できます。
  
- プロファイル セクションへのアクセス。
    
- フォルダーまたはメッセージのコピー。 詳細については、「メッセージまたは [フォルダーのコピーまたは移動」を参照してください](copying-or-moving-a-message-or-a-folder.md)。
    
- 他のプロバイダーに属するオブジェクトへのアクセス。 詳細については、「Supporting [Object Access and Comparison」を参照してください](supporting-object-access-and-comparison.md)。 
    
- イベント通知の処理。 詳細については、「サポート イベント通知 [」を参照してください](supporting-event-notification.md)。
    
- メモリの割り当てと解放。
    
- 一意の識別子を取得します。
    
- オブジェクトの無効化。
    
- エラーの処理。
    
- メッセージ プリプロセッサの登録。 
    
- メッセージ配信レポートの準備。 
    
ログオン時に、MAPI は各サービス プロバイダーのプロバイダー オブジェクトのログオン メソッドを呼び出します。 アドレス帳プロバイダーの場合、MAPI は [IABProvider::Logon を呼び出します](iabprovider-logon.md)。 メッセージ ストア プロバイダーの場合、MAPI は [IMSProvider::Logon を呼び出します](imsprovider-logon.md)。 トランスポート プロバイダーの場合、MAPI は [IXPProvider::TransportLogon を呼び出します](ixpprovider-transportlogon.md)。 MAPI は、パラメーターの 1 つで適切なサポート オブジェクトへのポインターをこのメソッドに渡します。 ログオン メソッドは、ログオン オブジェクトをインスタンス化し、サポート オブジェクト ポインターを渡します。 ログオン オブジェクトは、必要に応じてサポート オブジェクト **の IUnknown::AddRef** メソッドを呼び出して保持します。 サービス プロバイダーのログオン プロセスの詳細については、「サービス プロバイダーの開始 [」を参照してください](starting-a-service-provider.md)。
  
クライアントがログオフすると、MAPI はログオン オブジェクトの logoff メソッドを呼び出します。 logoff メソッドは、サポート オブジェクトの **IUnknown::Release** メソッドを呼び出して、プロバイダーがサポート メソッドを呼び出す予定がなくなったかどうかを示します。 ログオンと同様に、logoff メソッドの名前は若干異なります。 [IABLogon インターフェイスと](iablogoniunknown.md) [IMSLogon](imslogoniunknown.md)インターフェイスには **Logoff メソッド** があります。[IXPLogon インターフェイス](ixplogoniunknown.md)には [TransportLogoff メソッド](ixplogon-transportlogoff.md)があります。 
  
メッセージ サービスエントリ ポイント関数は、ログオン試行が失敗した場合、またはクライアントが構成要求を開始MAPI_E_UNCONFIGUREDエラーが発生した場合に呼び出されます。 MAPI は、構成サポート オブジェクトをインスタンス化し、構成が変更されるプロバイダーまたは構成が変更されるプロバイダーのいずれかのメッセージ サービス エントリ ポイント関数を呼び出します。 他のサポート オブジェクトとは異なり、構成サポート オブジェクトは、エントリ ポイント関数が返されるまで有効です。メッセージ サービスは、これらのオブジェクトを保持するために **これらのオブジェクトの AddRef** メソッドを呼び出しません。 
  
通常、MAPI はプロバイダーのメッセージ サービス エントリ ポイント関数を呼び出しますが、プロバイダーに呼び出しを求めらる場合があります。 これは、クライアントがプロバイダーの [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) メソッドを呼び出して、プロバイダーに構成プロパティ シートの表示を求めるメッセージを表示するときに発生することがあります。 **SettingsDialog は** [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) を呼び出して、メッセージ サービス エントリ ポイント関数に渡す構成サポート オブジェクトを取得する必要があります。 
  
[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドは、MAPI とリンクすることなく、メモリ割り当ておよび割り当て解除関数のアドレスを決定するために使用できます。 **GetMemAllocRoutines** を使用すると、割り当て関数呼び出しをデバッグ コードで囲み、メモリ リークの追跡も容易になります。 **GetMemAllocRoutines** を呼び出す場合は、パラメーターとして割り当て関数のアドレスを必要とする [CreateIProp](createiprop.md)関数を呼び出す前に呼び出してください。 
  
新しいアドレス帳またはメッセージ ストア オブジェクトを作成する必要がある場合は、オブジェクトの検索キーを作成して、そのオブジェクトのプロパティ [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md) **PR_SEARCH_KEY設定します**。 [IMAPISupport::NewUID](imapisupport-newuid.md)を呼び出して、検索キーの作成に使用する一意の識別子を取得します。 独自のハードコードされた [MAPIUID を使用しない](mapiuid.md)。 プロバイダーの **MAPIUID は** 、エントリ識別子にのみ使用する必要があります。 検索キーの作成の詳細については、「MAPI レコードと [検索キー」を参照してください](mapi-record-and-search-keys.md)。
  
クライアント アプリケーションは、1 つ以上の関連オブジェクトを解放せずにオブジェクトを解放できる場合があります。 このような場合、プロバイダーは、使用できない未発表のオブジェクトをレンダリングする必要があります。 これを行うには、プロバイダーはオブジェクトに接続されているリソースをすべて解放し [、IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) を呼び出してオブジェクトの vtable を無効にします。 **MakeInvalid** は、vtable の **IUnknown** メソッド **(QueryInterface、AddRef、** および **Release)** を標準の MAPI 実装に置き換え、他のすべてのメソッドが MAPI_E_INVALID_OBJECT を返します。  **MakeInvalid は** 、vtable 以外のすべてのオブジェクトのメモリも解放します。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

