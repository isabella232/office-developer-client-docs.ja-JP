---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350877"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クライアントがクライアントプロセスの高速シャットダウンを実行できるようにします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |[imapisession](imapisessioniunknown.md)オブジェクト  <br/> |
|実装元:  <br/> |MAPI サブシステム  <br/> |
|呼び出し元:  <br/> |MAPI クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIClientShutdown  <br/> |
|ポインターの種類:  <br/> |lpmapiclientshutdown  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |読み込み済みの mapi プロバイダーによって提供される高速シャットダウンのサポートを mapi サブシステムに対して照会します。  <br/> |
|[notifyprocessshutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |シャットダウンを続行する MAPI クライアントの意図を示します。  <br/> |
|[dofastshutdown](imapiclientshutdown-dofastshutdown.md) <br/> |クライアントプロセスをすぐに終了する MAPI クライアントの意図を示します。  <br/> |
   
## <a name="remarks"></a>解説

高速シャットダウンの目的は、mapi クライアントと、mapi の設定とデータを保存するために mapi クライアントがアクティブな mapi セッションを持つ、すべての読み込み済みの mapi プロバイダーを許可することです。 これにより、MAPI クライアントは、データ損失を発生させることなく、すべての外部参照を切断し、終了することができます。 高速シャットダウンを実行する必要がある MAPI クライアントは、 **IMAPIClientShutdown**インターフェイスを使用する必要があります。 MAPI クライアントは、任意の[imapisession](imapisessioniunknown.md)オブジェクトで IUnknown:: QueryInterface メソッドを呼び出すことによって、このインターフェイスへのポインターを取得できます。 
  
MAPI クライアントは、 **IMAPIClientShutdown:: queryfastshutdown**メソッドを呼び出して、常に高速シャットダウンを開始します。 mapi サブシステムは、読み込み済みの mapi プロバイダーがクライアントの高速シャットダウンをサポートしているかどうかを確認することによって、mapi クライアントのクエリに応答します。 管理者は、Windows レジストリ設定を使用して、MAPI クライアントが高速シャットダウンを続行するために必要なプロバイダーサポートのレベルを判断するのに役立てることができます。 詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。
  
高速シャットダウンを続行するには、クライアントは**IMAPIClientShutdown:: notifyprocessshutdown**メソッドを呼び出して、MAPI サブシステムにシャットダウンの意図を示します。 クライアントは**IMAPIClientShutdown::D ofastshutdown**メソッドを呼び出して、クライアントプロセスが直ちに終了したことを示します。 
  
高速シャットダウンの詳細については、「[高速シャットダウンの概要](fast-shutdown-overview.md)」を参照してください。 高速シャットダウンを正常に実行する方法については、「[ファストシャットダウンのベストプラクティス](best-practices-for-fast-shutdown.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)
  
[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

