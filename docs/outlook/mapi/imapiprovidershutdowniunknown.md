---
title: imapiprovidershutdown IUnknown
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
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322408"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi サブシステムが mapi クライアントの高速シャットダウンの mapi プロバイダーに通知できるようにして、mapi プロバイダーがシャットダウンに応答できるようにします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |プロバイダーオブジェクト: [ixpprovider](ixpprovideriunknown.md)、 [IABProvider](iabprovideriunknown.md)、または[IMSProvider](imsprovideriunknown.md) <br/> |
|実装元:  <br/> |MAPI プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI サブシステム  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|ポインターの種類:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |MAPI プロバイダーに対して、高速シャットダウンのサポートを照会します。  <br/> |
|[notifyprocessshutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |mapi クライアントが高速シャットダウンを実行することを mapi プロバイダーに示します。これにより、プロバイダーはデータ損失を防止するアクションを実行できるようになります。  <br/> |
|[dofastshutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |mapi プロバイダーに対して、mapi クライアントが直ちに終了していることを示します。したがって、データ損失を防止するために mapi プロバイダーは変更を保持します。  <br/> |
   
## <a name="remarks"></a>解説

高速シャットダウンを使用すると、クライアントとロードされた mapi プロバイダーが mapi の設定とデータを保存した後に、mapi クライアントが短時間でプロセスを終了することができます。 mapi クライアントは、常に高速シャットダウンを開始し、読み込み済みの mapi プロバイダーからの高速シャットダウンのサポートのために mapi サブシステムに対してクエリを実行する必要があります。 管理者は、ユーザーレベルで Windows レジストリを設定して、すべての MAPI クライアントの高速シャットダウンを可能にするために必要なプロバイダーサポートのレベルを指定することができます。 レジストリ設定の詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。 しかし、データ損失が発生することなく、高速なシャットダウンが正常に実行されるようにするには、MAPI プロバイダーが**imapiprovidershutdown**インターフェイスを実装する必要があります。 
  
クライアントの高速シャットダウンをサポートする必要がある mapi プロバイダーは、 **imapiprovidershutdown:: queryfastshutdown**メソッド内の mapi サブシステムに S_OK を返す必要があります。 mapi サブシステムが、 **imapiprovidershutdown:: notifyprocessshutdown**および**imapiprovidershutdown**を呼び出した場合、mapi プロバイダーは mapi の設定とデータを保存するために必要なアクションを実行する必要があります。クライアントの終了を準備します。 
  
クライアントの高速シャットダウンをサポートする必要がない MAPI プロバイダーは、まだ**imapiprovidershutdown**インターフェイスを実装していて、 **imapiprovidershutdown:: queryfastshutdown**メソッドが MAPI_E_NO_SUPPORT を返すようにしてください。 outlook を MAPI クライアントとして使用する場合、outlook は、すべての外部参照が終了するまで待機します。 
  
高速シャットダウンのためのユーザーの Windows レジストリ設定によっては、 **imapiprovidershutdown**インターフェイスを実装していないと、クライアントの高速シャットダウンが必ずしも妨げられるわけではありません。 
  
高速シャットダウンのプロセスの詳細については、「[高速シャットダウンの概要](fast-shutdown-overview.md)」を参照してください。 高速シャットダウンを正常に実行する方法については、「[ファストシャットダウンのベストプラクティス](best-practices-for-fast-shutdown.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)
  
[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

