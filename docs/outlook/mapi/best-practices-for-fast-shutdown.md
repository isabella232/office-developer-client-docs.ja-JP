---
title: 高速シャットダウンのベストプラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8c7225427b80d89c6dd8adfa85f7d91885850365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318145"
---
# <a name="best-practices-for-fast-shutdown"></a>高速シャットダウンのベストプラクティス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、管理者、mapi クライアント、および mapi プロバイダーが Windows レジストリ設定と高速シャットダウンインターフェイスを使用してクライアントのシャットダウン時のデータ損失を最小限に抑えるためのベストプラクティスについて説明します。
  
- mapi クライアントが高速シャットダウンを正常に実行するために、プロバイダープロセスがデータ損失を発生させないようにするには、まず、mapi クライアントは[IMAPIClientShutdown:: queryfastshutdown](imapiclientshutdown-queryfastshutdown.md)メソッドを呼び出す必要があります。 その後、クライアントは、MAPI サブシステムのサポートに基づいて、 [IMAPIClientShutdown:: notifyprocessshutdown](imapiclientshutdown-notifyprocessshutdown.md)および[IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md)メソッドを実行する必要があります。の**戻り値によって示されています。IMAPIClientShutdown:: queryfastshutdown**。 MAPI クライアントとして、Microsoft Outlook は**IMAPIClientShutdown:: notifyprocessshutdown**または**IMAPIClientShutdown:** : **IMAPIClientShutdown:: queryfastshutdown**がエラーを返す場合は、次のように呼び出しを行いません。 管理者が Windows レジストリで高速シャットダウンを無効にした場合、MAPI サブシステムは**IMAPIClientShutdown:: queryfastshutdown**に MAPI_E_NO_SUPPORT を返します。 この場合、mapi サブシステムは、すぐにクライアントプロセスの終了の mapi プロバイダーに通知しません。 そのため、mapi クライアントがこのエラーを無視して、高速シャットダウンが行われ、すべての外部参照が切断されると、読み込まれたすべての mapi プロバイダーでデータが失われます。 
    
- MAPI プロバイダーは、クライアントが終了する前に、クライアントが外部参照を切断したことによるデータ損失を回避するために必要な手順を実行するために、 [imapiprovidershutdown: IUnknown](imapiprovidershutdowniunknown.md)インターフェイスを実装する必要があります。 プロバイダーは、プライマリデータストアにデータを保存するために必須ではないすべてのものを延期する必要があります。 たとえば、トランスポートプロバイダーは、新しいメールをチェックする不必要なバックグラウンド操作を延期する必要があります。アドレス帳プロバイダーは、サーバーからの最新の変更のダウンロードを延期する必要があります。また、ストアプロバイダーは、次のようなメンテナンスタスクを延期する必要があります。圧縮またはインデックス作成。 
    
- MAPI クライアントを閉じるとすぐに終了するようにする場合は、プロバイダーが使用しない限り、高速シャットダウンを可能にする既定のレジストリ設定を使用する必要があります。
    
- mapi クライアントが IMAPIClientShutdown を呼び出すと、 **:D ofastshutdown**は、 [MAPIUninitialize](mapiuninitialize.md)関数を含む mapi に対して追加の呼び出しを行うことはできません。 クライアントは、クライアントプロセスの残りの期間に MAPI を使用しないようにする必要があります。 
    
- MAPI クライアントは、プロバイダーの**imapiprovidershutdown**インターフェイスを直接呼び出すことはできません。 MAPI クライアントは常に[IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インターフェイスを使用する必要があります。 
    
- 読み込み時に高速シャットダウンが使用されないようにする必要がある場合は、MAPI プロバイダーが**imapiprovidershutdown**インターフェイスを実装し、 **imapiprovidershutdown:: queryfastshutdown**メソッドの MAPI_E_NO_SUPPORT を返す必要があります。 ただし、Outlook などの MAPI クライアントの場合、クライアントが高速シャットダウンを中止し、シャットダウンにかかる時間が長くなります。 
    
## <a name="see-also"></a>関連項目



[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)
  
[高速シャットダウンの概要](fast-shutdown-overview.md)
  
[高速シャットダウンのユーザーオプション](fast-shutdown-user-options.md)

