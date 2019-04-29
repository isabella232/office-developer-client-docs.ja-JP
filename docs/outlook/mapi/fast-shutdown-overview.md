---
title: 高速シャットダウンの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: 8c33214b04e7c41eab173196c09f145c20ddf219
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427207"
---
# <a name="fast-shutdown-overview"></a>高速シャットダウンの概要

**適用対象**: Outlook 2013 | Outlook 2016 
  
高速シャットダウンは、クライアントがアクティブな mapi セッションを持っているすべてのプロバイダーに、クライアントプロセスが終了する前にデータおよび設定を保存するように通知する、mapi クライアントのメカニズムです。 このトピックでは、高速シャットダウンの基本的なメカニズムについて説明します。 

microsoft outlook 2010 以降では、microsoft outlook 2013 を含む現在、MAPI サブシステムは[IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インターフェイスを提供しています。 Outlook およびその他の MAPI クライアントは、クライアントプロセスを終了するための既定のメカニズムとして、高速シャットダウンを採用できます。 クライアントコンピューターの Windows レジストリのユーザーレベルの設定により、そのコンピューター上のそのユーザーのすべての MAPI クライアントに対する高速シャットダウンの導入が制御されます。 レジストリ設定の詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。
  
MAPI クライアントで高速シャットダウンを導入する必要がある場合は、 **IMAPIClientShutdown: IUnknown**インターフェイスを使用する必要があります。 クライアントがシャットダウンしようとする場合の一般的なイベントの例を次に示します。 
  
1. mapi クライアントは、 [IMAPIClientShutdown:: queryfastshutdown](imapiclientshutdown-queryfastshutdown.md)メソッドを呼び出してシャットダウンを開始し、mapi サブシステムが高速シャットダウンをサポートしているかどうかを判断します。 
    
2. MAPI サブシステムは、次の手順を使用して、クライアントの**IMAPIClientShutdown:: queryfastshutdown**呼び出しに対して使用可能な高速シャットダウンサポートで応答します。 
    
    1. mapi サブシステムは、mapi クライアントプロセスがアクティブな mapi セッションを持つ mapi プロバイダーごとに、imapiprovidershutdown: [: queryfastshutdown](imapiprovidershutdown-queryfastshutdown.md)メソッドを呼び出します。これは、プロバイダーが[imapiprovidershutdown: IUnknown](imapiprovidershutdowniunknown.md)を実装している場合です。インターフェイス. 
        
       > [!NOTE]
       >  mapi サブシステムは常に、次の順序で mapi プロバイダーに対して、 **imapiprovidershutdown: IUnknown**インターフェイスを通じて mapi プロバイダーに対してクエリを実行し、それぞれの mapi セッションで通知します。
       > 1. トランスポートプロバイダー
       > 2. アドレス帳プロバイダー
       > 3. ストアプロバイダー 
    
    2. クライアントコンピューターでのそのユーザーの高速シャットダウンのレジストリ設定に応じて、MAPI サブシステムは**IMAPIClientShutdown:: queryfastshutdown**に対して適切なリターンコードを指定します。 戻り値のコードは、S_OK または MAPI_E_NO_SUPPORT のいずれかです。
        
    3. mapi クライアントは[IMAPIClientShutdown:: notifyprocessshutdown](imapiclientshutdown-notifyprocessshutdown.md)メソッドを呼び出して、mapi サブシステムにシャットダウンの意図を示します。 
        
    4. mapi サブシステムは、読み込まれた mapi プロバイダーごとに、mapi クライアントがシャットダウンすることを示します。 **imapiprovidershutdown: IUnknown**インターフェイスを実装しているプロバイダーの MAPI サブシステムは、対応する[imapiprovidershutdown:: notifyprocessshutdown](imapiprovidershutdown-notifyprocessshutdown.md)メソッドを呼び出します。 
        
    5. mapi クライアントは[IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md)メソッドを呼び出して、クライアントプロセスが直ちに終了したことを mapi サブシステムに示します。 
        
    6. mapi サブシステムは、mapi クライアントプロセスを終了する、読み込まれた各 mapi プロバイダーを示します。 **imapiprovidershutdown: IUnknown**インターフェイスを実装しているプロバイダーの MAPI サブシステムは、対応する[imapiprovidershutdown::D ofastshutdown](imapiprovidershutdown-dofastshutdown.md)メソッドを呼び出します。 この時点で、これらの mapi プロバイダーは、データや設定の保存など、必要なすべての操作が完了したことを、mapi クライアントが直ちにすべての参照を切断して終了することを確認する必要があります。 
    
## <a name="see-also"></a>関連項目

- [MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)
- [高速シャットダウンのユーザーオプション](fast-shutdown-user-options.md)
- [高速シャットダウンのためのベスト プラクティス](best-practices-for-fast-shutdown.md)

