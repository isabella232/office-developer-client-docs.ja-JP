---
title: ログオン オブジェクトを実装します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e23c73931c9051b61d30b7ea7e9c54d06a4d9c33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800911"
---
# <a name="implementing-a-logon-object"></a>ログオン オブジェクトを実装します。

  
  
**適用されます**: Outlook 
  
すべてのアドレス帳、メッセージ ・ ストア、およびトランスポート プロバイダーは、 [IABProvider::Logon](iabprovider-logon.md)、 [IMSProvider::Logon](imsprovider-logon.md)、または[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)の実装の一部としてのログオン オブジェクトをインスタンス化します。 ログオン オブジェクトでは、MAPI クライアントの要求のためのメソッドを実装します。 サービス プロバイダーの種類によっては、ログオン オブジェクトは次のインターフェイスのいずれかでサポートされます。 
  
|**ログオン オブジェクトのインタ フェース**|**サービス プロバイダー**|
|:-----|:-----|
|[IABLogon: IUnknown](iablogoniunknown.md) <br/> |アドレス帳プロバイダー  <br/> |
|[IMSLogon: IUnknown](imslogoniunknown.md) <br/> |メッセージ ストア プロバイダー  <br/> |
|[IXPLogon: IUnknown](ixplogoniunknown.md) <br/> |トランスポート プロバイダー  <br/> |
   
アドレス帳とメッセージ ・ ストア プロバイダーの実装次の機能で、ログオン オブジェクト。
  
- イベント通知 (**アドバイズ**と**Unadvise**メソッド) をサポートします。 イベント通知の詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 ログオン オブジェクトの通知をサポートの詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。 
    
- (**CompareEntryIDs**メソッド) エントリ識別子を比較します。 エントリ id の詳細については、 [MAPI エントリの識別子](mapi-entry-identifiers.md)を参照してください。 **CompareEntryIDs**メソッドをログオン オブジェクトのエントリ id を比較することに関する詳細については、[オブジェクトへのアクセスをサポートしているとの比較](supporting-object-access-and-comparison.md)を参照してください。
    
- 追加のエラー情報 (**GetLastError**メソッド) にアクセスします。 MAPI でのエラー処理の詳細については、 [MAPI でエラーが処理](error-handling-in-mapi.md)を参照してください。 
    
- サービス プロバイダー (**OpenEntry**メソッド) が実装されているオブジェクトにアクセスします。 詳細については、[オブジェクトへのアクセスをサポートしているとの比較](supporting-object-access-and-comparison.md)を参照してください。
    
- 状態オブジェクト (**OpenStatusEntry**メソッド) にアクセスします。 ステータス オブジェクトの詳細については、 [MAPI オブジェクトのステータス](mapi-status-objects.md)を参照してください。 状態オブジェクトを実装する詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。
    
- ログオフ プロセス (**ログオフ**の方法)。 詳細については、[シャット ダウン、サービス ・ プロバイダー](shutting-down-a-service-provider.md)を参照してください。
    
プロバイダーが、アドレス帳プロバイダーの場合は、以下の方法と関連する機能も実装します。
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md)の新しい受信者を作成するためにサポートしているテンプレートの一覧を提供します。 詳細については、[一時テーブル](one-off-tables.md)または[一時テーブル プロバイダーを実装する](implementing-a-provider-one-off-table.md)を参照してください。
    
- データが含まれる受信者の実装へのアクセスを提供する[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)は、ホストのアドレス帳に存在します。 詳細については、[外部のアドレス帳プロバイダーとしての機能](acting-as-a-foreign-address-book-provider.md)を参照してください。 
    
- [IABLogon::PrepareRecips](iablogon-preparerecips.md)の適切なプロパティが受信者のリスト内の受信者のすべての利用可能であることを確認します。 詳細については、 [IABLogon::PrepareRecips](iablogon-preparerecips.md)を参照してください。 
    
トランスポート プロバイダーのログオン オブジェクトを実装して、 [IXPLogon: IUnknown](ixplogoniunknown.md)、サービス ・ プロバイダーの他の型によって実装されているログオン オブジェクトとはまったく異なります。 他のログオン オブジェクトと共通の 2 つのみの機能がある: [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md)メソッドを通じて状態オブジェクト、および[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)メソッドからのログオフ操作へのアクセス。 トランスポート プロバイダーは、そのログオン オブジェクトで次の独自の機能を実装します。 
  
- ([IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッド) のアドレスの種類を登録します。 アドレスの種類を登録の詳細については、[トランスポート プロバイダーおよび MAPI スプーラーの運用モデル](transport-provider-and-mapi-spooler-operational-model.md)を参照してください。
    
- メッセージの転送 ([IXPLogon::StartMessage](ixplogon-startmessage.md)、 [IXPLogon::EndMessage](ixplogon-endmessage.md)、および[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッド) をコントロールできます。 詳細については、[メッセージ受信モデル](message-reception-model.md)、 [MAPI スプーラーと対話する](interacting-with-the-mapi-spooler.md)、および[メッセージの送信モデル](message-submission-model.md)を参照してください。
    
- 内部状態の検証 ([IXPLogon::ValidateState](ixplogon-validatestate.md)メソッド)。 
    
- ([IXPLogon::FlushQueues](ixplogon-flushqueues.md)メソッド) を必要に応じてメッセージをアップロードまたはダウンロードできます。 詳細については、 [FlushQueues メソッドを実装する](implementing-the-flushqueues-method.md)を参照してください。
    
- 保留中のメッセージ ([IXPLogon::Poll](ixplogon-poll.md)メソッド) を照会する機能です。 詳細については、[メッセージ受信のモデル](message-reception-model.md)を参照してください。
    
- アイドル状態の検出 ([IXPLogon::Idle](ixplogon-idle.md)メソッド)。 
    
- MAPI スプーラーを無効 ([IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッド) との相互作用します。 
    
## <a name="see-also"></a>関連項目



[サービス プロバイダーへのログオンを実装します。](implementing-service-provider-logon.md)

