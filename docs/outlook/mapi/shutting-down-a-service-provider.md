---
title: サービス プロバイダーのシャットダウン
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 70db0b0a62568cc499cf915634756bb422ae82ca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567196"
---
# <a name="shutting-down-a-service-provider"></a>サービス プロバイダーのシャットダウン

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアントがセッションを終了し、すべてのアクティブなサービス プロバイダーをシャット ダウンするには、 [IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出すと、MAPI は順に次メソッドを呼び出します。 
  
- アドレス帳プロバイダーの[IABLogon::Logoff](iablogon-logoff.md)にします。 
    
- メッセージ ストア プロバイダーの[IMSLogon::Logoff](imslogon-logoff.md)にします。 
    
- トランスポート プロバイダーの[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)にします。 
    
これらのメソッドでは、ような実装があります。 ログオフ メソッドを実行する主要なタスクは次のとおりです。
  
- すべてのサブオブジェクトを含め、開いているオブジェクトと状態オブジェクトを解放します。
    
- メソッド サポート オブジェクトの[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)の参照カウントをデクリメントします。 
    
- プロバイダーの登録済みの[MAPIUID](mapiuid.md)構造体のすべてを削除しています。 
    
- ステータスの表に、プロバイダーの行を削除しています。
    
- 次のように、リソースのクリーンアップに関連するすべてのタスクを実行するには。
    
  - リモート サーバーとの接続を終了しています。
    
  - ログオン オブジェクトの参照をデクリメントする操作をカウントします。
    
  - ログオン オブジェクトをプロバイダーが格納されているログオン オブジェクトの一覧から削除しています。
    
  - デバッグ モードでのメモリをリークしているオブジェクトを検索するのにはトレースを発行します。
    
ログオフ メソッドから制御が戻るとき、MAPI が次に呼び出されます。
  
- ログオン オブジェクトの**リ ス**の方法です。 
    
- プロバイダー オブジェクトの最終的なクリーンアップ タスクを実行するのにはメソッドを**シャット ダウン**します。 、プロバイダーの種類によって次の方法のいずれかが呼び出されます。 
    
  - アドレス帳プロバイダーの[IABProvider::Shutdown](iabprovider-shutdown.md) 
    
  - メッセージ ストア プロバイダーの[IMSProvider::Shutdown](imsprovider-shutdown.md) 
    
  - トランスポート プロバイダーの[IXPProvider::Shutdown](ixpprovider-shutdown.md) 
    
- プロバイダー オブジェクトの**リ ス**の方法です。 
    
プロバイダーがメッセージ ・ ストアの場合は、 [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)へのクライアント呼び出しがシャット ダウン処理を開始してもできます。 **StoreLogoff**は、1 つの特定のメッセージ ストア プロバイダーをシャット ダウンし、セッションに影響を与えません。 メッセージ ストア プロバイダーだけをこの方法でシャット ダウンをできます。特定のアドレス帳またはトランスポート プロバイダーをシャット ダウンする明示的な方法はありません。 の**StoreLogoff**に応答する方法についての情報を呼び出して、[シャット ダウン、メッセージ ストア プロバイダー](shutting-down-a-message-store-provider.md)を参照してください。
  
MAPI は、Win32 API 関数**終わった**が、最後のアクティブなクライアントが[MAPIUninitialize](mapiuninitialize.md)を呼び出した後に行われた呼び出しを呼び出すと、プロバイダーの DLL がアンロードされるされます。 この時点で、シャット ダウン、サービス ・ プロバイダーが完了しましたが。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

