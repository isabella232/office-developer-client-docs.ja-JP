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
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339208"
---
# <a name="shutting-down-a-service-provider"></a>サービス プロバイダーのシャットダウン

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントが [IMAPISession::Logoff](imapisession-logoff.md) メソッドを呼び出してセッションを終了し、すべてのアクティブなサービス プロバイダーをシャットダウンすると、MAPI は次のメソッドを呼び出します。 
  
- [アドレス帳プロバイダーの IABLogon::Logoff。](iablogon-logoff.md) 
    
- [メッセージ ストア プロバイダーの IMSLogon::Logoff。](imslogon-logoff.md) 
    
- [IXPLogon::TransportLogoff for](ixplogon-transportlogoff.md) transport providers. 
    
これらのメソッドは、同様の実装を持っています。 ログオフ メソッドが実行する主なタスクは次のとおりです。
  
- サブオブジェクトや状態オブジェクトを含む、開いているすべてのオブジェクトを解放します。
    
- サポート オブジェクトの [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) メソッドを呼び出して、参照カウントをデクレメントします。 
    
- プロバイダーの登録済み [MAPIUID 構造体をすべて削除](mapiuid.md) します。 
    
- 状態テーブル内のプロバイダーの行を削除します。
    
- 次のようなリソースのクリーンアップに関連するタスクを実行します。
    
  - リモート サーバーとの接続を終了する。
    
  - ログオン オブジェクトの参照カウントをデクレメントします。
    
  - プロバイダーが格納するログオン オブジェクトの一覧からログオン オブジェクトを削除する。
    
  - デバッグ モードでは、メモリがリークしたオブジェクトを検索するトレースを発行します。
    
logoff メソッドが返された場合、MAPI は次を呼び出します。
  
- ログオン オブジェクトの **IUnknown::Release** メソッド。 
    
- プロバイダー オブジェクトの **Shutdown** メソッドを使用して、最終的なクリーンアップ タスクを実行します。 プロバイダーの種類に応じて、次のいずれかのメソッドが呼び出されます。 
    
  - [IABProvider::アドレス帳](iabprovider-shutdown.md) プロバイダーのシャットダウン 
    
  - [IMSProvider::メッセージ ストア](imsprovider-shutdown.md) プロバイダーのシャットダウン 
    
  - [IXPProvider::トランスポート](ixpprovider-shutdown.md) プロバイダーのシャットダウン 
    
- プロバイダー オブジェクトの **IUnknown::Release** メソッド。 
    
プロバイダーがメッセージ ストアの場合は [、IMsgStore::StoreLogoff](imsgstore-storelogoff.md) へのクライアント呼び出しでもシャットダウン プロセスが開始されます。 **StoreLogoff は** 、1 つの特定のメッセージ ストア プロバイダーをシャットダウンし、セッションには影響しません。 このメソッドを使用してシャットダウンできるのは、メッセージ ストア プロバイダーのみです。特定のアドレス帳またはトランスポート プロバイダーをシャットダウンする明示的な方法はありません。 **StoreLogoff** 呼び出しに応答する方法の詳細については、「メッセージ ストア プロバイダーのシャットダウン [」を参照してください](shutting-down-a-message-store-provider.md)。
  
MAPI が Win32 API 関数 **FreeLibrary** を呼び出す場合、プロバイダーの DLL はアンロードされます。最後のアクティブなクライアントが [MAPIUninitialize](mapiuninitialize.md)を呼び出した後に行われた呼び出しです。 この時点で、サービス プロバイダーはシャットダウンを終了します。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

