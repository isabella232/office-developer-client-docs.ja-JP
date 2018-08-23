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
ms.openlocfilehash: 9fb372e504eaeb55861b09c4151956fb102c08f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577150"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアント プロセスの高速シャット ダウンを実行するために MAPI クライアントを有効にします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |[IMAPISession](imapisessioniunknown.md)オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI サブシステム  <br/> |
|によって呼び出されます。  <br/> |MAPI クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIClientShutdown  <br/> |
|ポインターの型。  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |クエリ、MAPI サブシステムの高速シャット ダウンをサポートして読み込まれている MAPI プロバイダーによって提供されます。  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |続行するのには MAPI クライアントの意図をシャット ダウンを示します。  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |MAPI クライアントのクライアントのプロセスを即座に終了するという意図を示しています。  <br/> |
   
## <a name="remarks"></a>注釈

高速シャット ダウンでは、MAPI クライアントと、読み込まれている MAPI プロバイダーにすると、MAPI クライアントは、MAPI の設定とデータを保存するのにはアクティブな MAPI セッションを許可します。 これにより、MAPI クライアントをすべての外部参照を切断して、データの損失を発生させることがなく終了します。 高速シャット ダウンを行うに必要な MAPI クライアントでは、 **IMAPIClientShutdown**インターフェイスを使用する必要があります。 MAPI クライアントは、 [IMAPISession](imapisessioniunknown.md)オブジェクトの IUnknown::QueryInterface メソッドを呼び出して、このインターフェイスへのポインターを取得できます。 
  
MAPI クライアントは、常に**IMAPIClientShutdown::QueryFastShutdown**メソッドを呼び出すことによって、高速シャット ダウンを開始します。 MAPI サブシステムは、読み込まれている MAPI プロバイダーがクライアントの高速シャット ダウンをサポートするかどうかを確認することによって、MAPI クライアントのクエリに応答します。 管理者は、高速シャット ダウンを続行するのには MAPI クライアントに必要なプロバイダーのサポートのレベルを判断するための Windows レジストリ設定を使用できます。 詳細については、[高速シャット ダウンのユーザー オプション](fast-shutdown-user-options.md)を参照してください。
  
高速シャット ダウンを続行するには、クライアントは、MAPI サブシステムにシャット ダウンするという意図を示すために**IMAPIClientShutdown::NotifyProcessShutdown**メソッドを呼び出します。 クライアントは、クライアント プロセスがすぐに終了することを示すために**IMAPIClientShutdown::DoFastShutdown**メソッドを呼び出します。 
  
高速シャット ダウンの詳細については、[高速シャット ダウンの概要](fast-shutdown-overview.md)を参照してください。 高速シャット ダウンが正常に実行する方法の詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)
  
[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

