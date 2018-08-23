---
title: サポート オブジェクトの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7f43a50d08daedc623fa1e4570eafa5d58be71f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577437"
---
# <a name="support-object-overview"></a>サポート オブジェクトの概要

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI をサポート オブジェクトを実装するオブジェクトを提供する、 [IMAPISupport: IUnknown](imapisupportiunknown.md)インタ フェースは、ログオン時にすべてのサービス プロバイダーとすべてのメッセージ サービスの構成中にします。 
  
サポート オブジェクトは、クライアントによってアクセスできません。MAPI によって実装されており、サービス ・ プロバイダーによってのみ呼び出されます。 **IMAPISupport**インターフェイスは、Mapispi.h ヘッダー ファイルで指定します。 その識別子は IID_IMAPISup で、そのポインター型は LPMAPISUP です。 サポート オブジェクトによって MAPI プロパティが公開されることはありません。 
  
プロバイダーは、プロバイダーのメッセージ サービスのエントリ関数が呼び出される回数または時間の MAPI ログオン プロバイダーの数に応じて、1 つ以上のサポート オブジェクトを得ることができます。 通常、プロバイダーは、セッションごとに少なくとも 1 回記録されます。 アドレス帳およびトランスポート プロバイダーは、クライアントがそれらを要求するプロファイル エントリを持つセッションを起動するたびにログオンします。 メッセージ ストア プロバイダーは、クライアントが、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドを呼び出すたびにログオンします。 
  
場合は複数のログオン セッションでは、ことができますいずれかを保持し、サポートの各オブジェクトを個別に使用するを保持し、最初のものだけを使用して、各後続のサポート オブジェクトを破棄すること。 サポート オブジェクトを保持するには、 **IUnknown::AddRef**メソッドを呼び出します。 セッション全体で保持する必要があるサポート オブジェクトで**AddRef**を呼び出すことは、非常に重要です。呼び出しが行われない限り、MAPI はサポート オブジェクトを解放し、そのメモリを解放します。 
  
サポート オブジェクトの目的は、かなり多数のプロバイダーで一般的に使用するメソッドの実装を提供すること。 サポートの各オブジェクトには、プロバイダーは、プロバイダーを使用しているプロファイル] セクションで実行中のセッションなどの独自のインスタンスとセッションのエラー情報を特定のコンテキストのデータも含まれています。 
  
サポート オブジェクトの 4 つの種類があります: 各 (アドレス帳、メッセージ ・ ストア、およびトランスポート) は、主なプロバイダーの種類と構成のサポートのいずれかのいずれかです。 
  
MAPI は、その使用法に関連付けられているメソッドの実装を含めることによって、サポートの各オブジェクトをカスタマイズします。 サポートのすべてのオブジェクトには、 [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)などのいくつかのメソッドの実装が含まれます。 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)などの他のメソッドの実装は、特定のサポートのオブジェクトにのみ適用されます。 のみメッセージ ストアと、トランスポート プロバイダーは、このメソッドを使用できます。アドレス帳プロバイダーまたはメッセージ サービスを呼び出すことと、MAPI は、MAPI_E_NO_SUPPORT を返します。
  
サポート オブジェクトは、次のような多くのタスクを実行する使用できます。
  
- プロファイル セクションへのアクセス。
    
- フォルダーまたはメッセージをコピーしています。 詳細については、[コピーまたは移動するメッセージまたはフォルダー](copying-or-moving-a-message-or-a-folder.md)を参照してください。
    
- 他のプロバイダーに属しているオブジェクトにアクセスします。 詳細については、[オブジェクトへのアクセスをサポートしているとの比較](supporting-object-access-and-comparison.md)を参照してください。 
    
- イベント通知を処理します。 詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。
    
- 割り当てとメモリを解放します。
    
- 一意の識別子を取得します。
    
- オブジェクトを無効にします。
    
- エラーを処理します。
    
- プリプロセッサのメッセージを登録しています。 
    
- メッセージの配信レポートを準備しています。 
    
ログオン時に、MAPI は、各サービス プロバイダーのプロバイダー オブジェクトのログオン メソッドを呼び出します。 アドレス帳プロバイダーでは、MAPI は、 [IABProvider::Logon](iabprovider-logon.md)を呼び出します。 メッセージ ストア プロバイダーでは、MAPI は、 [IMSProvider::Logon](imsprovider-logon.md)を呼び出します。 トランスポート プロバイダーでは、MAPI は、 [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)を呼び出します。 MAPI は、このメソッドのパラメーターのいずれかで適切なサポート オブジェクトへのポインターを渡します。 ログオン方法には、サポート オブジェクトへのポインターを渡すこと、ログオン オブジェクトがインスタンス化します。 ログオン オブジェクトは、必要な場合に、その維持のサポート オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。 サービス プロバイダーの詳細については、ログオン プロセスは、[サービス プロバイダーの起動](starting-a-service-provider.md)を参照してください。
  
クライアントがログオフすると、MAPI は、ログオン オブジェクトのログオフのメソッドを呼び出します。 ログオフ メソッドでは、プロバイダーがサポートされている方法のいずれかを呼び出すため不要になった意図を示すためにサポート オブジェクトの**リ ス**のメソッドを呼び出します。 同様に、ログオンは、ログオフの方法は、わずかに異なる名前を持ちます。 [IABLogon](iablogoniunknown.md)および[IMSLogon](imslogoniunknown.md)インタ フェースがある**ログオフ**の方法です。[IXPLogon](ixplogoniunknown.md)インターフェイスには、 [TransportLogoff](ixplogon-transportlogoff.md)メソッドがあります。 
  
メッセージ サービスのエントリ ポイント関数は、MAPI_E_UNCONFIGURED エラーが発生したか、クライアント構成要求を開始すると、ログオンの試行が失敗したときに呼び出されます。 MAPI では、構成のサポート オブジェクトをインスタンス化し、未構成のプロバイダーまたはプロバイダーの構成は変更するのいずれかのメッセージ サービスのエントリ ポイント関数を呼び出します。 オブジェクトと異なり、その他のサポート、構成のサポート オブジェクトは、有効なエントリ ポイントの関数の戻り値までの間だけメッセージ サービスは、それらを保持するのには、これらのオブジェクトの**AddRef**メソッドを呼び出さないようにします。 
  
通常、MAPI プロバイダーのメッセージ サービスのエントリ ポイント関数を呼び出すは、呼び出しを行うプロバイダーが要求する場合があります。 これは、クライアントが、構成のプロパティ シートを表示するのにはプロバイダーに確認する、プロバイダーの[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドを呼び出すときに発生します。 **SettingsDialog**は、メッセージ サービスのエントリ ポイント関数に渡すことができる、構成のサポート オブジェクトを取得する[IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md)を呼び出す必要があります。 
  
[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドは、MAPI を使用してリンクすることがなくメモリの割り当ておよび割り当て解除関数のアドレスを決定するために使用します。 **GetMemAllocRoutines**を使用しても簡単にコードのデバッグの割り当て関数の呼び出しを囲むと、メモリ リークを追跡します。 呼び出す場合は**GetMemAllocRoutines**を勧め、パラメーターとして割り当て関数のアドレスを必要とする、 [CreateIProp](createiprop.md)関数を呼び出す前にするようにします。 
  
作成する必要がある場合、新しいアドレス帳やメッセージ ストア オブジェクトを作成した、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティで、オブジェクトの検索キーを設定します。 検索キーの作成に使用する一意の識別子を取得するのには[IMAPISupport::NewUID](imapisupport-newuid.md)を呼び出します。 独自ハード コードされた[MAPIUID](mapiuid.md)を使用しません。 プロバイダーの**MAPIUID**は、エントリの識別子にのみ使用してください。 検索キーを作成することに関する詳細については、 [MAPI の記録と検索キー](mapi-record-and-search-keys.md)を参照してください。
  
クライアント アプリケーションは、1 つまたは複数の関連オブジェクトのボタンを押したままオブジェクトを解放することができる場合があります。 このような場合、プロバイダーは、解放されていないオブジェクトが使用できなく必要があります。 これを行うには、プロバイダーはすべてのオブジェクトに接続されているリソースを解放し、オブジェクトの vtable を無効にする[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)を呼び出して、します。 **MakeInvalid**は、vtable の**IUnknown**のメソッド (**QueryInterface**、 **AddRef**、および**Release**) を標準的な MAPI 実装に置き換えます、MAPI_E_INVALID_OBJECT を取得する他のすべての方法は、します。 **MakeInvalid**は、vtable 以外のすべてのオブジェクトのメモリも解放されます。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

