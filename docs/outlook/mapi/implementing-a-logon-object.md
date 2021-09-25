---
title: Logon オブジェクトの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4fbc8dbbb3ed82ec4b5f519b96a25ac674df1119
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584305"
---
# <a name="implementing-a-logon-object"></a>Logon オブジェクトの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのアドレス帳、メッセージ ストア、およびトランスポート プロバイダーは[、IABProvider::Logon](iabprovider-logon.md) [、IMSProvider::Logon、](imsprovider-logon.md)[または IXPProvider::TransportLogon](ixpprovider-transportlogon.md)の実装の一環としてログオン オブジェクトをインスタンス化します。 ログオン オブジェクトは、MAPI サービス クライアント要求に役立つメソッドを実装します。 サービス プロバイダーの種類に応じて、ログオン オブジェクトは次のいずれかのインターフェイスをサポートします。 
  
|**ログオン オブジェクト インターフェイス**|**サービス プロバイダー**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |アドレス帳プロバイダー  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |メッセージ ストア プロバイダー  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |トランスポート プロバイダー  <br/> |
   
アドレス帳とメッセージ ストア プロバイダーは、ログオン オブジェクトに次の機能を実装します。
  
- イベント通知のサポート (**アドバイス** メソッドと **Unadvise** メソッド)。 イベント通知の概要については [、「MAPI でのイベント通知」を参照してください](event-notification-in-mapi.md)。 ログオン オブジェクトでの通知のサポートの詳細については、「サポート イベント通知」 [を参照してください](supporting-event-notification.md)。 
    
- エントリ識別子の比較 (**CompareEntryIDs** メソッド)。 エントリ識別子の一般的な情報については [、「MAPI エントリ識別子」を参照してください](mapi-entry-identifiers.md)。 ログオン オブジェクトの **CompareEntryIDs** メソッドでのエントリ識別子の比較の詳細については、「Supporting Object Access and [Comparison」を参照してください](supporting-object-access-and-comparison.md)。
    
- 追加のエラー情報 **(GetLastError メソッド** ) へのアクセス。 MAPI でのエラーの処理の詳細については、「MAPI での [エラー処理」を参照してください](error-handling-in-mapi.md)。 
    
- サービス プロバイダー **(OpenEntry** メソッド) によって実装されたオブジェクトへのアクセス。 詳細については、「Supporting [Object Access and Comparison」を参照してください](supporting-object-access-and-comparison.md)。
    
- status オブジェクト **(OpenStatusEntry メソッド** ) へのアクセス。 状態オブジェクトの一般的な情報については [、「MAPI Status Objects」を参照してください](mapi-status-objects.md)。 status オブジェクトの実装の詳細については、「Status [Object Implementation」を参照してください](status-object-implementation.md)。
    
- ログオフ プロセス (**Logoff** メソッド)。 詳細については、「サービス プロバイダーの [シャットダウン」を参照してください](shutting-down-a-service-provider.md)。
    
プロバイダーがアドレス帳プロバイダーの場合は、次のメソッドと関連する機能も実装します。
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) を使用して、新しい受信者の作成をサポートするテンプレートの一覧を提供します。 詳細については [、「One-Off Tables」](one-off-tables.md) または [「Implementing a Provider One-Off Table」を参照してください](implementing-a-provider-one-off-table.md)。
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) を使用して、ホスト アドレス帳プロバイダーにデータが存在する受信者の実装へのアクセスを提供します。 詳細については、「外部アドレス [帳プロバイダーとして機能する」を参照してください](acting-as-a-foreign-address-book-provider.md)。 
    
- [IABLogon::P repareRecips](iablogon-preparerecips.md) を使用して、受信者リスト内のすべての受信者に適切なプロパティを使用できます。 詳細については [、「IABLogon::P repareRecips」を参照してください](iablogon-preparerecips.md)。 
    
[IXPLogon : IUnknown](ixplogoniunknown.md)を実装するトランスポート プロバイダーのログオン オブジェクトは、他の種類のサービス プロバイダーによって実装されるログオン オブジェクトとは大きな違いがあります。 他のログオン オブジェクトと共通する機能は 2 つのみです [。IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) メソッドを使用した状態オブジェクトへのアクセスと [、IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) メソッドを使用したログオフ操作です。 トランスポート プロバイダーは、ログオン オブジェクトに次の一意の機能を実装します。 
  
- アドレスの種類の登録[(IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッド)。 アドレスの種類の登録の詳細については、「トランスポート プロバイダーと MAPI スプーラー運用モデル [」を参照してください](transport-provider-and-mapi-spooler-operational-model.md)。
    
- メッセージ送信の制御[(IXPLogon::StartMessage](ixplogon-startmessage.md) [、IXPLogon::EndMessage、](ixplogon-endmessage.md)[および IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッド)。 詳細については [、「Message Reception Model](message-reception-model.md)」、MAPI スプー [ラー](interacting-with-the-mapi-spooler.md)との対話、およびメッセージ送信 [モデルを参照してください](message-submission-model.md)。
    
- 内部状態の検証[(IXPLogon::ValidateState](ixplogon-validatestate.md) メソッド)。 
    
- オンデマンドでメッセージをダウンロードまたはアップロードする機能[(IXPLogon::FlushQueues](ixplogon-flushqueues.md) メソッド)。 詳細については [、「FlushQueues メソッドの実装」を参照してください](implementing-the-flushqueues-method.md)。
    
- 保留中のメッセージをクエリする機能[(IXPLogon::P oll](ixplogon-poll.md) メソッド)。 詳細については、「Message [Reception Model」を参照してください](message-reception-model.md)。
    
- アイドル状態の検出[(IXPLogon::Idle](ixplogon-idle.md) メソッド)。 
    
- MAPI スプーラーとの対話[(IXPLogon::TransportNotify](ixplogon-transportnotify.md) メソッド)。 
    
## <a name="see-also"></a>関連項目



[サービス プロバイダー ログオンの実装](implementing-service-provider-logon.md)

