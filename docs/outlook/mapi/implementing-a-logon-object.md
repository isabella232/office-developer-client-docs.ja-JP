---
title: ログオンオブジェクトの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332845"
---
# <a name="implementing-a-logon-object"></a>ログオンオブジェクトの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのアドレス帳、メッセージストア、およびトランスポートプロバイダーは、 [IABProvider:: logon](iabprovider-logon.md)、 [IMSProvider:: logon](imsprovider-logon.md)、または[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)の実装の一環として、ログオンオブジェクトをインスタンス化します。 Logon オブジェクト MAPI サービスクライアントからの要求を支援するメソッドを実装します。 サービスプロバイダーの種類に応じて、ログオンオブジェクトは次のいずれかのインターフェイスをサポートします。 
  
|**ログオンオブジェクトインターフェイス**|**サービスプロバイダー**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |アドレス帳プロバイダー  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |メッセージストアプロバイダー  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |トランスポートプロバイダー  <br/> |
   
アドレス帳およびメッセージストアプロバイダーは、ログオンオブジェクトに次の機能を実装します。
  
- イベント通知のサポート (**アドバイズ**および**アドバイズ**中止メソッド)。 イベント通知の概要については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 ログオンオブジェクトでの通知のサポートの詳細については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。 
    
- エントリ識別子の比較 (**compareentryids**メソッド)。 エントリ識別子に関する一般的な情報については、「 [MAPI エントリ識別子](mapi-entry-identifiers.md)」を参照してください。 ログオンオブジェクトの**compareentryids**メソッドでのエントリ識別子の比較の詳細については、「[オブジェクトのアクセスと比較のサポート](supporting-object-access-and-comparison.md)」を参照してください。
    
- 追加のエラー情報 (**GetLastError**メソッド) へのアクセス。 mapi でのエラー処理の詳細については、「 [mapi でのエラー処理](error-handling-in-mapi.md)」を参照してください。 
    
- サービスプロバイダ (**openentry**メソッド) によって実装されたオブジェクトへのアクセス。 詳細については、「[オブジェクトのアクセスと比較のサポート](supporting-object-access-and-comparison.md)」を参照してください。
    
- status オブジェクト (**openstatusentry**メソッド) へのアクセス。 状態オブジェクトの概要については、「 [MAPI 状態オブジェクト](mapi-status-objects.md)」を参照してください。 状態オブジェクトの実装に関する具体的な情報については、「 [status オブジェクトの実装](status-object-implementation.md)」を参照してください。
    
- ログオフプロセス (**logoff**メソッド)。 詳細については、「[サービスプロバイダーをシャットダウンする](shutting-down-a-service-provider.md)」を参照してください。
    
プロバイダーがアドレス帳プロバイダーの場合は、次のメソッドと関連する機能も実装します。
  
- [IABLogon:: getoneofftable](iablogon-getoneofftable.md)新しい受信者の作成に対してサポートされているテンプレートの一覧を提供します。 詳細については、「 [1 回限りのテーブル](one-off-tables.md)の実装」または「[プロバイダーの1回限りのテーブルの実装](implementing-a-provider-one-off-table.md)」を参照してください。
    
- [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)を使用して、ホストアドレス帳プロバイダーにデータが存在する受信者の実装へのアクセスを提供します。 詳細については、「[外部アドレス帳プロバイダーとして機能する](acting-as-a-foreign-address-book-provider.md)」を参照してください。 
    
- [IABLogon: reparerecips](iablogon-preparerecips.md)を使用して、受信者リスト内のすべての受信者に対して適切なプロパティが利用可能であることを確認します。 詳細については、「 [IABLogon::P reparerecips](iablogon-preparerecips.md)」を参照してください。 
    
[IXPLogon: IUnknown](ixplogoniunknown.md)を実装するトランスポートプロバイダーのログオンオブジェクトは、他の種類のサービスプロバイダーによって実装されるログオンオブジェクトとは大きく異なります。 他のログオンオブジェクトとの共通点は2つあります。 [IXPLogon:: openstatusentry](ixplogon-openstatusentry.md)メソッドを使用した状態オブジェクトへのアクセス、および[IXPLogon:: transportlogoff](ixplogon-transportlogoff.md)メソッドによるログオフ操作。 トランスポートプロバイダーは、それぞれのログオンオブジェクトに、次のような固有の機能を実装します。 
  
- アドレスの種類の登録 ([IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッド)。 アドレスの種類の登録の詳細については、「 [Transport Provider and MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md)」を参照してください。
    
- メッセージ転送の制御 ([IXPLogon:: startmessage](ixplogon-startmessage.md), [IXPLogon:: endmessage](ixplogon-endmessage.md), and [IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッド)。 詳細については、「[メッセージ受信モデル](message-reception-model.md)」、「 [MAPI スプーラーとの対話](interacting-with-the-mapi-spooler.md)」、および「[メッセージ送信モデル](message-submission-model.md)」を参照してください。
    
- 内部状態の検証 ([IXPLogon:: validatestate](ixplogon-validatestate.md)メソッド)。 
    
- 必要に応じてメッセージをダウンロードまたはアップロードする機能 ([IXPLogon:: flushqueues](ixplogon-flushqueues.md)メソッド)。 詳細については、「 [flushqueues メソッドの実装](implementing-the-flushqueues-method.md)」を参照してください。
    
- 保留中のメッセージを照会する機能 ([IXPLogon::P oll](ixplogon-poll.md)メソッド)。 詳細については、「[メッセージ受信モデル](message-reception-model.md)」を参照してください。
    
- アイドル状態の検出 ([IXPLogon:: idle](ixplogon-idle.md)メソッド)。 
    
- MAPI スプーラー ([IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッド) との相互作用。 
    
## <a name="see-also"></a>関連項目



[サービスプロバイダーログオンの実装](implementing-service-provider-logon.md)

