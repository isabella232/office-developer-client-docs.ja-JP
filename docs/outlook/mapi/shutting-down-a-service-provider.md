---
title: サービスプロバイダーのシャットダウン
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
# <a name="shutting-down-a-service-provider"></a>サービスプロバイダーのシャットダウン

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントが[imapisession:: Logoff](imapisession-logoff.md)メソッドを呼び出してセッションを終了し、すべてのアクティブなサービスプロバイダーをシャットダウンすると、次のメソッドが呼び出されます。 
  
- [IABLogon:: ログオフ](iablogon-logoff.md)アドレス帳プロバイダー。 
    
- [IMSLogon:: ログオフ](imslogon-logoff.md)するメッセージストアプロバイダー。 
    
- [IXPLogon::](ixplogon-transportlogoff.md)トランスポートプロバイダーの transportlogoff。 
    
これらのメソッドには、同様の実装があります。 logoff メソッドが実行する主要なタスクは次のとおりです。
  
- サブオブジェクトおよびステータスオブジェクトを含む、開いているオブジェクトをすべて解放します。
    
- サポートオブジェクトの[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出して、参照カウントをデクリメントします。 
    
- プロバイダーの登録済みの[MAPIUID](mapiuid.md)構造体をすべて削除します。 
    
- 状態テーブルのプロバイダーの行を削除します。
    
- リソースのクリーンアップに関連するすべてのタスクを実行します。たとえば、次のようになります。
    
  - リモートサーバーとの接続を終了します。
    
  - ログオンオブジェクトの参照カウントをデクリメントします。
    
  - プロバイダーが格納するログオンオブジェクトの一覧から、ログオンオブジェクトを削除します。
    
  - デバッグモードで、リークしたメモリがあるオブジェクトを検索するためのトレースを発行します。
    
logoff メソッドが戻ると、MAPI は次のように呼び出します。
  
- ログオンオブジェクトの**IUnknown:: Release**メソッド。 
    
- 最終的なクリーンアップタスクを実行するには、プロバイダーオブジェクトの**Shutdown**メソッドを使用します。 プロバイダーの種類に応じて、次のいずれかのメソッドが呼び出されます。 
    
  - [IABProvider::](iabprovider-shutdown.md)アドレス帳プロバイダーのシャットダウン 
    
  - [IMSProvider::](imsprovider-shutdown.md)メッセージストアプロバイダーのシャットダウン 
    
  - [ixpprovider:: Shutdown](ixpprovider-shutdown.md) for transport providers 
    
- プロバイダーオブジェクトの**IUnknown:: Release**メソッド。 
    
プロバイダーがメッセージストアの場合、 [IMsgStore:: storelogoff](imsgstore-storelogoff.md)へのクライアント呼び出しでも、シャットダウンプロセスが開始されます。 **storelogoff**は、1つの特定のメッセージストアプロバイダーをシャットダウンし、セッションには影響を与えません。 このメソッドを使用すると、メッセージストアプロバイダーのみをシャットダウンできます。特定のアドレス帳またはトランスポートプロバイダーをシャットダウンする明示的な方法はありません。 **storelogoff**呼び出しに応答する方法については、「[メッセージストアプロバイダーのシャットダウン](shutting-down-a-message-store-provider.md)」を参照してください。
  
MAPI が Win32 API 関数**FreeLibrary**を呼び出すときに、プロバイダーの DLL がアンロードされます。最後にアクティブなクライアントが[MAPIUninitialize](mapiuninitialize.md)を呼び出した後で行われます。 この時点で、サービスプロバイダーはシャットダウンを終了しています。 
  
## <a name="see-also"></a>関連項目



[MAPI サービスプロバイダー](mapi-service-providers.md)

