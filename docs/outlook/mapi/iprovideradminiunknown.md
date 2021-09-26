---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 96f1c66980adebfb85b1e513df3a6ff236cf5776
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620556"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスのサービス プロバイダーと動作します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |プロバイダー管理オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IProviderAdmin  <br/> |
|ポインターの種類:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |プロバイダー管理オブジェクト [に発生](mapierror.md) した以前のエラーに関する情報を含む MAPIERROR 構造体を返します。  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |メッセージ サービスのプロバイダー テーブル 、メッセージ サービス内のサービス プロバイダーの一覧へのアクセスを提供します。  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |サービス プロバイダーをメッセージ サービスに追加します。  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |メッセージ サービスからサービス プロバイダーを削除します。  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |現在のプロファイルからプロファイル セクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは [、IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)メソッドを呼び出すことによって **、IProviderAdmin** インターフェイスへのポインターを取得できます。メッセージ サービスのエントリ ポイント関数が呼び出された場合、サービス プロバイダーは **IProviderAdmin** ポインターを渡されます。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

