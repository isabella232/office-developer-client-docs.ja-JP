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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435335"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クライアントがクライアント プロセスの高速シャットダウンを実行できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |[IMAPISession](imapisessioniunknown.md) オブジェクト  <br/> |
|実装元:  <br/> |MAPI サブシステム  <br/> |
|呼び出し元:  <br/> |MAPI クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIClientShutdown  <br/> |
|ポインターの種類:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |読み込まれた MAPI プロバイダーによって提供される高速シャットダウンのサポートを MAPI サブシステムに照会します。  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |シャットダウンを続行する MAPI クライアントの意図を示します。  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |MAPI クライアントがクライアント プロセスを直ちに終了する意図を示します。  <br/> |
   
## <a name="remarks"></a>注釈

高速シャットダウンの目的は、MAPI クライアントと、MAPI クライアントが MAPI 設定とデータを保存するアクティブな MAPI セッションを持つ読み込まれた MAPI プロバイダーを許可することです。 これにより、MAPI クライアントは、すべての外部参照を切断し、データ損失を引き起こすことなく終了できます。 高速シャットダウンを実行する必要がある MAPI クライアントは **、IMAPIClientShutdown インターフェイスを使用する必要** があります。 MAPI クライアントは [、IMAPISession](imapisessioniunknown.md) オブジェクトで IUnknown::QueryInterface メソッドを呼び出すことによって、このインターフェイスへのポインターを取得できます。 
  
MAPI クライアントは **、IMAPIClientShutdown::QueryFastShutdown** メソッドを呼び出すことによって、常に高速シャットダウンを開始します。 MAPI サブシステムは、読み込まれた MAPI プロバイダーがクライアントの高速シャットダウンをサポートするかどうかを確認して、MAPI クライアントのクエリに応答します。 管理者は、Windows設定を使用して、MAPI クライアントが高速シャットダウンを続行するために必要なプロバイダー サポートのレベルを判断できます。 詳細については、「Fast [Shutdown User Options」を参照してください](fast-shutdown-user-options.md)。
  
高速シャットダウンを続行するために、クライアントは **IMAPIClientShutdown::NotifyProcessShutdown** メソッドを呼び出して、MAPI サブシステムにシャットダウンの意図を示します。 次に、クライアントは **IMAPIClientShutdown::D oFastShutdown** メソッドを呼び出して、クライアント プロセスが直ちに終了しているかどうかを示します。 
  
高速シャットダウンの詳細については、「Fast [Shutdown Overview」を参照してください](fast-shutdown-overview.md)。 高速シャットダウンを正常に実行する方法については、「高速シャットダウンの [ベスト プラクティス」を参照してください](best-practices-for-fast-shutdown.md)。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)
  
[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

