---
title: メッセージ ストア プロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339201"
---
# <a name="shutting-down-a-message-store-provider"></a>メッセージ ストア プロバイダーのシャットダウン

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーがメッセージ ストア プロバイダーの場合は、次のいずれかの方法でシャットダウンできます。
  
- クライアントまたは MAPI スプーラーが [IMsgStore::StoreLogoff を呼び出す場合](imsgstore-storelogoff.md)。 **StoreLogoff** を使用してメッセージ ストア プロバイダーをシャットダウンすると、シャットダウンが順序付けされ、制御された方法で実行されます。 
    
- クライアントが [IMAPISession::Logoff を呼び出す場合](imapisession-logoff.md)。 
    
**IMsgStore::StoreLogoff** の実装は [、IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)を呼び出して、MAPI がシャットダウンされたことを通知し、関連するトランスポート プロバイダーをログオフする必要があります。 **IMsgStore::StoreLogoff が** 返された場合、その呼び出し元はメッセージ ストアの [IUnknown::Release メソッドを呼び出](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)します。 サポート オブジェクト **の****IUnknown::Release** メソッドを呼び出して、この Release メソッドを実装します。 
  
MAPI は、メッセージ ストアの **IUnknown::Release** の実装で次のタスクを実行します。 
  
1. メッセージ ストア プロバイダーによって登録されている [MAPIUID](mapiuid.md) 構造をすべて削除します。 
    
2. メッセージ ストア プロバイダーの行を状態テーブルから削除します。
    
3. [IMSLogon::Logoff](imslogon-logoff.md)を呼び出して、開いているすべてのオブジェクト、サブオブジェクト、および状態オブジェクトを解放します。 
    
4. [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)を呼び出して、メッセージ ストア プロバイダーのログオン オブジェクトを解放します。 
    
一部のクライアントでは **、IMsgStore::StoreLogoff** への呼び出しを省略し、メッセージ ストアの **IUnknown::Release** メソッドへの呼び出しでメッセージ ストア プロバイダーのシャットダウンを開始する場合があります。 このような状況では **、StoreLogoff** を呼び出さずにシャットダウンを実行すると、順序が低く制御されます。 この可能性を処理し **、IMAPISupport::StoreLogoffTransports** への呼び出しが発生したかどうかを追跡するために、メッセージ ストアの Release メソッドを記述します。  **StoreLogoffTransports は、** シャットダウン プロセス中に 1 回呼び出す必要があります。 Release メソッドで **StoreLogoffTransports** がまだ呼び出されていないことを検出した場合は、このフラグを使用して呼びLOGOFF_ABORTします。 
  
## <a name="see-also"></a>関連項目



[サービス プロバイダーのシャットダウン](shutting-down-a-service-provider.md)

