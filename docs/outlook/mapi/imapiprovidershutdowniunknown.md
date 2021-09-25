---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5fa47b972be4ed58de052757545d505381e78cbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625539"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI サブシステムが MAPI クライアントの高速シャットダウンを MAPI プロバイダーに通知して、MAPI プロバイダーがシャットダウンに応答できます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |プロバイダー オブジェクト: [IXPProvider、IABProvider、](ixpprovideriunknown.md)または[IMSProvider](imsprovideriunknown.md) [](iabprovideriunknown.md) <br/> |
|実装元:  <br/> |MAPI プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI サブシステム  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|ポインターの種類:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |MAPI プロバイダーに高速シャットダウンのサポートを照会します。  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |MAPI クライアントが高速シャットダウンを実行し、プロバイダーがデータ損失を防止するアクションを実行できるよう、MAPI プロバイダーに対して示します。  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |MAPI クライアントが直ちに終了し、MAPI プロバイダーがデータ損失を防ぐために変更を保持する MAPI プロバイダーを示します。  <br/> |
   
## <a name="remarks"></a>注釈

高速シャットダウンにより、MAPI クライアントは、クライアントと読み込まれた MAPI プロバイダーが MAPI 設定とデータを保存した後、短時間でプロセスを終了できます。 MAPI クライアントは常に高速シャットダウンを開始し、読み込まれた MAPI プロバイダーからの高速シャットダウンのサポートを MAPI サブシステムに照会する必要があります。 管理者は、ユーザー レベルWindowsレジストリを設定して、すべての MAPI クライアントの高速シャットダウンを許可するために必要なプロバイダー サポートのレベルを指定できます。 レジストリ設定の詳細については、「Fast Shutdown [User Options」を参照してください](fast-shutdown-user-options.md)。 ただし、データ損失なしで高速シャットダウンが正常に行われるには、MAPI プロバイダーが **IMAPIProviderShutdown インターフェイスを実装する必要** があります。 
  
クライアントの高速シャットダウンをサポートする必要がある MAPI プロバイダーは **、IMAPIProviderShutdown::QueryFastShutdown** メソッドの MAPI サブシステムにS_OKを返す必要があります。 MAPI サブシステムが後で **IMAPIProviderShutdown::NotifyProcessShutdown** と **IMAPIProviderShutdown::D oFastShutdown** メソッドを呼び出す場合、MAPI プロバイダーは MAPI 設定とデータを保存し、クライアントの終了に備える必要なアクションを実行する必要があります。 
  
クライアントの高速シャットダウンをサポートする必要のない MAPI プロバイダーは **、IMAPIProviderShutdown** インターフェイスを実装し **、IMAPIProviderShutdown::QueryFastShutdown** メソッドが MAPI_E_NO_SUPPORT を返す必要があります。 MAPI Outlookとして使用すると、Outlook前にすべての外部参照が解放されるのを待つ必要があります。 
  
高速シャットダウン用のユーザーの Windows レジストリ設定によっては **、IMAPIProviderShutdown** インターフェイスを実装しない場合でも、クライアントの高速シャットダウンが必ずしも妨げであるとは限りません。 
  
高速シャットダウンのプロセスの詳細については、「Fast Shutdown Overview 」 [を参照してください](fast-shutdown-overview.md)。 高速シャットダウンを正常に実行する方法については、「Fast Shutdown の [ベスト プラクティス」を参照してください](best-practices-for-fast-shutdown.md)。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)
  
[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

