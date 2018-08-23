---
title: 高速シャットダウンのためのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0d9e7caf43bcee654aa92652e94bc8c2ebba18e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799752"
---
# <a name="best-practices-for-fast-shutdown"></a>高速シャットダウンのためのベスト プラクティス

  
  
**適用対象**: Outlook 
  
このトピックでは、管理者、MAPI クライアントでは、および MAPI プロバイダーがクライアントのシャット ダウン時にデータの損失を最小限に抑えるため、Windows レジストリの設定と高速シャット ダウン インターフェイスを使用するためのベスト プラクティスを推奨します。
  
- プロバイダーのプロセスは、データの損失を引き起こさないように、高速シャット ダウンを正常に実行するための MAPI クライアントの MAPI クライアントは最初に[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドを呼び出す必要があります。 クライアントし、どうすべき、高速シャット ダウンは、MAPI サブシステムのサポートに基づいた[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)と[IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md)メソッドを使用して**の戻り値によって示されるIMAPIClientShutdown::QueryFastShutdown**。 MAPI クライアントとして Microsoft Outlook は呼び出しません**IMAPIClientShutdown::NotifyProcessShutdown**または**IMAPIClientShutdown::DoFastShutdown** **IMAPIClientShutdown::QueryFastShutdown**には、エラーが返されます。 管理者は Windows レジストリの高速シャット ダウンを無効にした場合、MAPI サブシステムは**IMAPIClientShutdown::QueryFastShutdown**に MAPI_E_NO_SUPPORT を返します。 この例では、MAPI サブシステムが通知 MAPI プロバイダーを直接クライアント プロセスの終了。 したがって、MAPI クライアントは、このエラー コードを無視、高速シャット ダウンの操作を行いますに進み、すべての外部参照を切断、読み込まれているすべての MAPI プロバイダーはデータの損失があります。 
    
- MAPI プロバイダーを実装する必要があります、 [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)クライアントを終了する前に、外部参照を切断するクライアントによるデータの損失を避けるために、タイムリーかつ必要な手順を実行するインターフェイス。 プロバイダーは、プライマリ ・ データ ・ ストアにデータを保存するのには重要ではないその他のすべてを延期する必要があります。 たとえば、トランスポート プロバイダーは、新しいメールは、アドレス帳プロバイダーが、サーバーから最新の変更のダウンロードを延期する必要があります。 を確認する不要なバック グラウンド操作を延期する必要があり。、ストア プロバイダーは次のように保守タスクを延期する必要があります。最適化するか、インデックスを作成します。 
    
- MAPI クライアントがそれらを閉じるとすぐに終了したいユーザーは、プロバイダーの選択しない限り、高速シャット ダウンを有効にするデフォルトのレジストリ設定を使用してください。
    
- MAPI クライアントは、 **IMAPIClientShutdown::DoFastShutdown**を呼び出すと MAPI、 [MAPIUninitialize](mapiuninitialize.md)関数を含む、追加の呼び出しは作成しないでください。 クライアントは、クライアント プロセスの有効期間の残りの部分に MAPI を使用しないでください。 
    
- MAPI クライアントは、プロバイダーの**IMAPIProviderShutdown**インターフェイスを直接呼び出す必要があります。 常に MAPI クライアントを使用する必要があります、 [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インタ フェースです。 
    
- MAPI プロバイダーが読み込まれるときに、その高速シャット ダウンは使用しないことを確認する場合は、 **IMAPIProviderShutdown**インターフェイスを実装し、 **IMAPIProviderShutdown::QueryFastShutdown**メソッドの MAPI_E_NO_SUPPORT を返すする必要があります。 ただし、Outlook などの MAPI クライアントはこれにより、クライアントが高速シャット ダウンを中止し、シャット ダウンに長い時間がかかります。 
    
## <a name="see-also"></a>関連項目



[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)
  
[高速シャットダウンの概要](fast-shutdown-overview.md)
  
[高速シャットダウンのユーザー オプション](fast-shutdown-user-options.md)

