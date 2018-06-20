---
title: メッセージ ストア プロバイダーをシャット ダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b5c9874ca465bb0ebed62f218d1512feb1a2f9ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803917"
---
# <a name="shutting-down-a-message-store-provider"></a>メッセージ ストア プロバイダーをシャット ダウン

  
  
**適用されます**: Outlook 
  
プロバイダーがメッセージ ストア プロバイダーの場合は、それをシャット ダウンできる次の方法のいずれかで。
  
- クライアントまたは MAPI スプーラーを呼び出すと[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)を。 規則的かつ制御された方法で発生するシャット ダウンは、 **StoreLogoff**のメッセージ ストア プロバイダーをシャット ダウンします。 
    
- クライアントは、 [IMAPISession::Logoff](imapisession-logoff.md)を呼び出すとします。 
    
シャット ダウン、、関連するトランスポート プロバイダーを記録する必要があることを示す MAPI を通知するために[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)を呼び出すことによって**IMsgStore::StoreLogoff**の実装を開始する必要があります。 **IMsgStore::StoreLogoff**が返されるとき、呼び出し元は、メッセージ ・ ストアの[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)のメソッドを呼び出します。 サポート オブジェクト**が**メソッドを呼び出して、**このメソッド**を実装します。 
  
MAPI は、メッセージ ・ ストアの**リ ス**の実装で、次のタスクを実行します。 
  
1. メッセージ ストア プロバイダーが登録されている[MAPIUID](mapiuid.md)の構造体のすべてを削除します。 
    
2. 状態テーブルからには、メッセージ ストア プロバイダーの行を削除します。
    
3. すべての開いているオブジェクトは、下位オブジェクト、および状態オブジェクトを解放するのには[IMSLogon::Logoff](imslogon-logoff.md)を呼び出します。 
    
4. メッセージ ストア プロバイダーのログオン オブジェクトを解放する[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)を呼び出します。 
    
一部のクライアントは、 **IMsgStore::StoreLogoff**、メッセージ ストアの**** メソッドの呼び出しでは、メッセージ ストア プロバイダーのシャット ダウンを開始する呼び出しを省略可能性があります。 **StoreLogoff**への呼び出しがない状況ではこれらのシャット ダウンは、あまり規則的で制御されました。 この可能性を処理し、 **IMAPISupport::StoreLogoffTransports**への呼び出しが発生したかどうかの追跡、メッセージ ・ ストアの**Release**のメソッドを記述します。 **StoreLogoffTransports**は、シャット ダウン処理中に 1 回呼び出す必要があります。 検出した場合、 **Release**のメソッドである**StoreLogoffTransports**がまだ呼び出されていない、LOGOFF_ABORT フラグを指定して呼び出すことです。 
  
## <a name="see-also"></a>関連項目



[サービス プロバイダーをシャット ダウン](shutting-down-a-service-provider.md)

