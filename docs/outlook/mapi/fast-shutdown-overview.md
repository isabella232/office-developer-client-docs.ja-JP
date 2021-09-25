---
title: 高速シャットダウンの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: 49b14c6d627ed90f716eaa607b0e9421662c5ab7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567663"
---
# <a name="fast-shutdown-overview"></a>高速シャットダウンの概要

**適用対象**: Outlook 2013 | Outlook 2016 
  
高速シャットダウンは、MAPI クライアントがクライアント プロセスのクイック シャットダウンを開始するメカニズムであり、クライアントがアクティブな MAPI セッションを持つすべてのプロバイダーに通知して、クライアント プロセスが終了する前にデータと設定を保存します。 このトピックでは、高速シャットダウンの基本的なメカニズムについて説明します。 

MAPI サブシステムは、Microsoft Outlook 2010から開始し[Microsoft Outlook 2013、IMAPIClientShutdown : IUnknown インターフェイスを提供](imapiclientshutdowniunknown.md)します。 Outlook MAPI クライアントは、クライアント プロセスを終了するための既定のメカニズムとして高速シャットダウンを採用できます。 クライアント コンピューターの Windows レジストリのユーザー レベルの設定は、そのコンピューター上のすべての MAPI クライアントに対する高速シャットダウンの採用を制御します。 レジストリ設定の詳細については、「Fast [Shutdown User Options」を参照してください](fast-shutdown-user-options.md)。
  
MAPI クライアントが高速シャットダウンを採用する必要がある場合は **、IMAPIClientShutdown : IUnknown インターフェイスを使用する必要** があります。 クライアントがシャットダウンを試みる一般的なイベントの一般的なコースを次に示します。 
  
1. MAPI クライアントは [、IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) メソッドを呼び出して、MAPI サブシステムが高速シャットダウンをサポートするかどうかを判断して、シャットダウンを開始します。 
    
2. MAPI サブシステムは、次の手順を使用して、クライアントの **IMAPIClientShutdown::QueryFastShutdown** 呼び出しに対して、利用可能な高速シャットダウンサポートに応答します。 
    
    1. MAPI サブシステムは、MAPI クライアント プロセスがアクティブな MAPI セッションを持つ MAPI プロバイダーごとに [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) メソッドを呼び出します。プロバイダーが [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) インターフェイスを実装している場合。 
        
       > [!NOTE]
       >  MAPI サブシステムは常に **、IMAPIProviderShutdown : IUnknown** インターフェイスを使用して MAPI プロバイダーに対して次の順序でクエリを実行し、通知します。
       > 1. トランスポート プロバイダー
       > 2. アドレス帳プロバイダー
       > 3. ストア プロバイダー 
    
    2. クライアント コンピューター上のユーザーの高速シャットダウン レジストリ設定に応じて、MAPI サブシステムは **IMAPIClientShutdown::QueryFastShutdown** に適切な戻りコードを指定します。 戻りコードは、S_OKまたはMAPI_E_NO_SUPPORT。
        
    3. MAPI クライアントは [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) メソッドを呼び出して、シャットダウンの意図を MAPI サブシステムに示します。 
        
    4. MAPI サブシステムは、読み込まれた各 MAPI プロバイダーに対して、MAPI クライアントがシャットダウンを示します。 **IMAPIProviderShutdown : IUnknown** インターフェイスを実装したプロバイダーの場合、MAPI サブシステムは対応する [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md)メソッドを呼び出します。 
        
    5. MAPI クライアントは [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) メソッドを呼び出して、クライアント プロセスが直ちに終了している MAPI サブシステムに示します。 
        
    6. MAPI サブシステムは、読み込まれた各 MAPI プロバイダーに対して、MAPI クライアント プロセスが終了中かどうかを示します。 **IMAPIProviderShutdown : IUnknown** インターフェイスを実装したプロバイダーの場合、MAPI サブシステムは対応する [IMAPIProviderShutdown::D oFastShutdown](imapiprovidershutdown-dofastshutdown.md)メソッドを呼び出します。 この時点で、これらの MAPI プロバイダーは、データや設定の保存など、すべての必要なアクションが完了し、MAPI クライアントがすべての参照を直ちに切断して終了する準備が完了している必要があります。 
    
## <a name="see-also"></a>関連項目

- [MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)
- [Fast Shutdown User Options](fast-shutdown-user-options.md)
- [高速シャットダウンのためのベスト プラクティス](best-practices-for-fast-shutdown.md)

