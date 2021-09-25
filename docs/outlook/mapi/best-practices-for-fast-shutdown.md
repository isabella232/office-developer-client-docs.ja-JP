---
title: 高速シャットダウンのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 778bd83e1b75ffdf494bc56cf79a5393e0c975ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572096"
---
# <a name="best-practices-for-fast-shutdown"></a>高速シャットダウンのベスト プラクティス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、管理者、MAPI クライアント、MAPI プロバイダーが Windows レジストリ設定と高速シャットダウン インターフェイスを使用して、クライアントのシャットダウン時のデータ損失を最小限に抑えるためのベスト プラクティスを推奨します。
  
- プロバイダー プロセスでデータ損失が発生しないので、MAPI クライアントが高速シャットダウンを正常に実行するには、MAPI クライアントが最初に [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) メソッドを呼び出す必要があります。 クライアントは [、IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) および [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) メソッドを **、IMAPIClientShutdown::QueryFastShutdown** の戻り値で示される MAPI サブシステムの高速シャットダウンのサポートに基づいて続行する必要があります。 MAPI クライアントとして、Microsoft Outlook は **IMAPIClientShutdown::NotifyProcessShutdown** または **IMAPIClientShutdown::D oFastShutdown** を呼び出す必要はありません **。IMAPIClientShutdown::QueryFastShutdown** はエラーを返します。 管理者が Windows レジストリで高速シャットダウンを無効にした場合、MAPI サブシステムは **IMAPIClientShutdown::QueryFastShutdown** に MAPI_E_NO_SUPPORT を返します。 この場合、MAPI サブシステムは、MAPI プロバイダーに即時のクライアント プロセスの終了を通知しない。 したがって、MAPI クライアントがこのエラー戻りコードを無視し、高速シャットダウンを実行し、すべての外部参照を切断すると、読み込まれたすべての MAPI プロバイダーにデータ損失が発生します。 
    
- MAPI プロバイダーは [、IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) インターフェイスを実装して、クライアントがクライアントを終了する前に外部参照を切断した場合のデータ損失を回避するために、必要な手順を実行する必要があります。 プロバイダーは、データをプライマリ データ ストアに保存する必要がない他のすべてを延期する必要があります。 たとえば、トランスポート プロバイダーは、新しいメールをチェックする不要なバックグラウンド操作を延期し、アドレス帳プロバイダーはサーバーからの最近の変更のダウンロードを延期し、ストア プロバイダーは圧縮やインデックス作成などのメンテナンス タスクを延期する必要があります。 
    
- MAPI クライアントを閉じるとすぐに終了するユーザーは、プロバイダーがオプトアウトしない限り、高速シャットダウンを有効にする既定のレジストリ設定を使用する必要があります。
    
- MAPI クライアントが **IMAPIClientShutdown::D oFastShutdown** を呼び出したら [、MAPIUninitialize](mapiuninitialize.md) 関数を含む MAPI への追加の呼び出しを行う必要はありません。 クライアントは、クライアント プロセスの残りの期間、MAPI を使用しなく必要があります。 
    
- MAPI クライアントは、プロバイダーの **IMAPIProviderShutdown インターフェイスを直接呼び出す必要** があります。 MAPI クライアントは常に [IMAPIClientShutdown : IUnknown インターフェイスを使用する必要](imapiclientshutdowniunknown.md) があります。 
    
- MAPI プロバイダーが読み込み中に高速シャットダウンが使用されない必要がある場合は **、IMAPIProviderShutdown インターフェイスを実装し、IMAPIProviderShutdown::QueryFastShutdown** メソッドの MAPI_E_NO_SUPPORT を返す必要があります。  ただし、MAPI クライアント (Outlookなど) の場合、クライアントは高速シャットダウンを放棄し、シャットダウンに時間がかかります。 
    
## <a name="see-also"></a>関連項目



[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)
  
[高速シャットダウンの概要](fast-shutdown-overview.md)
  
[Fast Shutdown User Options](fast-shutdown-user-options.md)

