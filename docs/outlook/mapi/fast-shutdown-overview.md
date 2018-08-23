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
ms.openlocfilehash: 17b1307427af2c35fe9ba8ee40dc78958e6b4a21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800028"
---
# <a name="fast-shutdown-overview"></a>高速シャットダウンの概要

**適用対象**: Outlook 
  
高速シャット ダウンは、簡易クライアントがクライアント プロセスが終了する前に、データや設定を保存するのにはアクティブな MAPI セッションを持っているすべてのプロバイダーに通知する、クライアント プロセスのシャット ダウンを開始するのには MAPI クライアントのための機構です。 このトピックでは、高速シャット ダウンの基本的なメカニズムについて説明します。 

MAPI サブシステムは、Microsoft Outlook 2010 で起動して、Microsoft Outlook 2013 を含むようになりました、 [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インタ フェースです。 Outlook およびその他の MAPI クライアントは、クライアントのプロセスを終了するのには既定の機構として、高速シャット ダウンを採用することができます。 クライアント コンピューターの Windows レジストリにユーザー レベルの設定は、そのコンピューターでそのユーザーのすべての MAPI クライアント用の高速シャット ダウンの導入を制御します。 レジストリ設定の詳細については、[高速シャット ダウンのユーザー オプション](fast-shutdown-user-options.md)を参照してください。
  
それを使用する必要がある場合は、MAPI クライアントでは、高速シャット ダウンを採用する必要がある、 **IMAPIClientShutdown: IUnknown**インタ フェースです。 以下は、クライアントがシャット ダウンしようとするときのイベントの標準的なコースです。 
  
1. MAPI クライアントは、MAPI サブシステムが高速シャット ダウンをサポートしているかどうかを決定する[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドを呼び出すことによって、シャット ダウンを開始します。 
    
2. MAPI サブシステムは、次の手順を使用して、クライアントの**IMAPIClientShutdown::QueryFastShutdown**の呼び出しに使用可能な高速シャット ダウンのサポートを使用して応答します。 
    
    1. プロバイダーが実装されている場合、MAPI サブシステムが MAPI クライアント プロセスが、アクティブな MAPI セッションを各 MAPI プロバイダーの[IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md)メソッドを呼び出し、 [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)インタ フェースです。 
        
       > [!NOTE]
       >  MAPI サブシステムは、常にクエリを実行しからの MAPI プロバイダーに通知、 **IMAPIProviderShutdown: IUnknown**次の順序では、各 MAPI セッション内でのインターフェイス。
       > 1. トランスポート プロバイダー
       > 2. アドレス帳プロバイダー
       > 3. ストア プロバイダー 
    
    2. クライアント コンピューターでそのユーザーの高速シャット ダウンのレジストリ設定によっては、MAPI サブシステムは、 **IMAPIClientShutdown::QueryFastShutdown**への適切なリターン コードを指定します。 リターン コードは、S_OK または MAPI_E_NO_SUPPORT のいずれかです。
        
    3. MAPI クライアントは、MAPI サブシステムにシャット ダウンするという意図を示すために[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)メソッドを呼び出します。 
        
    4. MAPI サブシステムは、MAPI クライアントをシャット ダウンする読み込まれた各 MAPI プロバイダーに指示します。 これらのプロバイダーを実装しているため、 **IMAPIProviderShutdown: IUnknown**インタ フェースでは、MAPI サブシステムは対応する[IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md)メソッドを呼び出します。 
        
    5. MAPI クライアントは、MAPI サブシステムには、クライアント プロセスがすぐに終了することを示すために[IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md)メソッドを呼び出します。 
        
    6. MAPI サブシステムは、MAPI クライアントのプロセスを終了すること、読み込まれた各 MAPI プロバイダーを示します。 これらのプロバイダーを実装しているため、 **IMAPIProviderShutdown: IUnknown**インタ フェースでは、MAPI サブシステムは対応する[IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md)メソッドを呼び出します。 この時点では、これらの MAPI プロバイダーがデータと設定を保存するなど、必要なすべてのアクションがすぐにすべての参照を切断しを終了するには、MAPI クライアントのための準備の完了を確認する必要があります。 
    
## <a name="see-also"></a>関連項目

- [Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)
- [高速シャットダウンのユーザー オプション](fast-shutdown-user-options.md)
- [高速シャットダウンのためのベスト プラクティス](best-practices-for-fast-shutdown.md)

