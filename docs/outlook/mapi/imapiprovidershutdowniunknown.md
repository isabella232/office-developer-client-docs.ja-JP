---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 81b7b0c235f610e7aaa0c17ecd1760df5d382552
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587972"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI プロバイダーが、シャット ダウンに応答できるように、MAPI クライアントの高速シャット ダウンの MAPI プロバイダーに通知するために MAPI サブシステムを使用できます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |プロバイダー オブジェクト: [IXPProvider](ixpprovideriunknown.md)、 [IABProvider](iabprovideriunknown.md)、または[IMSProvider](imsprovideriunknown.md) <br/> |
|によって実装されます。  <br/> |MAPI プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI サブシステム  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIProviderShutdown  <br/> |
|ポインターの型。  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |クエリは高速シャット ダウンの MAPI プロバイダーをサポートします。  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |MAPI プロバイダーをプロバイダーは、データ損失を防ぐための処置を行うことができるように、高速シャット ダウンを行う MAPI クライアントを送信することを示します。  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |示します MAPI プロバイダーに MAPI クライアントが、すぐに終了している MAPI プロバイダーがデータの損失を防ぐために加えられた変更を永続化できるようにします。  <br/> |
   
## <a name="remarks"></a>注釈

高速シャット ダウンにより、MAPI クライアントは、短時間の処理を終了することを願って読み込まれていて、クライアント後 MAPI プロバイダーが、保存、MAPI の設定とデータです。 MAPI クライアントは常に高速シャット ダウンを開始して、MAPI のサブシステム読み込まれている MAPI プロバイダーから高速シャット ダウンをサポートするためにクエリを実行する必要があります。 管理者は、すべての MAPI クライアントの高速シャット ダウンを許可する必要があるプロバイダーのサポートのレベルを指定するのにはユーザー レベルで、Windows のレジストリを設定できます。 レジストリ設定の詳細については、[高速シャット ダウンのユーザー オプション](fast-shutdown-user-options.md)を参照してください。 ただし、データを失うことがなく正常に実行するのには高速シャット ダウンは、MAPI プロバイダーは、 **IMAPIProviderShutdown**インターフェイスを実装する必要があります。 
  
クライアントの高速シャット ダウンをサポートするために必要な MAPI プロバイダーは、MAPI サブシステムに、 **IMAPIProviderShutdown::QueryFastShutdown**メソッドで S_OK を返す必要があります。 MAPI プロバイダーが MAPI の設定とデータの保存に必要な操作を実行する必要があります MAPI サブシステムは、その後、 **IMAPIProviderShutdown::NotifyProcessShutdown**と**IMAPIProviderShutdown::DoFastShutdown**メソッドを呼び出しますと、クライアントの終了を準備します。 
  
クライアントの高速シャット ダウンをサポートするために必要としない MAPI プロバイダーの**IMAPIProviderShutdown**インターフェイスを実装し、MAPI_E_NO_SUPPORT を返す**IMAPIProviderShutdown::QueryFastShutdown**メソッドがある必要がありますも。 MAPI クライアントとして outlook でこのすべての外部参照を終了する前に解放するまで待機するように Outlook が発生します。 
  
によって**IMAPIProviderShutdown**インターフェイスを実装しない、高速シャット ダウンのレジストリ設定が必ずしもユーザーの Windows クライアントの高速シャット ダウンを防止します。 
  
高速シャット ダウンのプロセスの詳細については、[高速シャット ダウンの概要](fast-shutdown-overview.md)を参照してください。 高速シャット ダウンを正常に実行する方法の詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)
  
[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

