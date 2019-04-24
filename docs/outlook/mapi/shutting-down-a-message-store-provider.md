---
title: メッセージストアプロバイダーのシャットダウン
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
# <a name="shutting-down-a-message-store-provider"></a>メッセージストアプロバイダーのシャットダウン

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーがメッセージストアプロバイダーの場合は、次のいずれかの方法でシャットダウンできます。
  
- クライアントまたは MAPI スプーラーが[IMsgStore:: storelogoff](imsgstore-storelogoff.md)を呼び出したとき。 **storelogoff**を使用してメッセージストアプロバイダーをシャットダウンすると、シャットダウンが整然と制御された方法で発生します。 
    
- クライアントが[imapisession:: Logoff](imapisession-logoff.md)を呼び出すとき。 
    
**IMsgStore:: storelogoff**の実装は、 [imapisupport:: storelogofftransport](imapisupport-storelogofftransports.md)を呼び出して、シャットダウン中であることを MAPI に通知することによって開始します。これは、関連するすべてのトランスポートプロバイダーをログオフする必要があることを意味します。 **IMsgStore:: storelogoff**は、メッセージストアの[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出します。 サポートオブジェクトの**IUnknown:: release**メソッドを呼び出して、この**Release**メソッドを実装します。 
  
MAPI は、メッセージストアの**IUnknown:: Release**の実装で、次のタスクを実行します。 
  
1. メッセージストアプロバイダーによって登録されたすべての[MAPIUID](mapiuid.md)構造を削除します。 
    
2. メッセージストアプロバイダーの行を状態テーブルから削除します。
    
3. [IMSLogon:: Logoff](imslogon-logoff.md)を呼び出して、開いているすべてのオブジェクト、サブオブジェクト、およびステータスオブジェクトを解放します。 
    
4. [IUnknown:: release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)を呼び出して、メッセージストアプロバイダーのログオンオブジェクトを解放します。 
    
クライアントによっては、 **IMsgStore:: storelogoff**への呼び出しを省略して、メッセージストアの**IUnknown:: Release**メソッドへの呼び出しを使用して、メッセージストアプロバイダーのシャットダウンを開始する場合があります。 **storelogoff**への呼び出しなしで、このような状況下でのシャットダウンは、整然と制御されません。 この可能性を処理するために、メッセージストアの**Release**メソッドを記述し、 **: storelogofftransports**が発生したかどうかを追跡します。 **storelogofftransports**は、シャットダウンプロセス中に1回呼び出す必要があります。 **storelogofftransports**がまだ呼び出されていない**リリース**方法で検出した場合は、LOGOFF_ABORT フラグを使用して呼び出します。 
  
## <a name="see-also"></a>関連項目



[サービスプロバイダーのシャットダウン](shutting-down-a-service-provider.md)

