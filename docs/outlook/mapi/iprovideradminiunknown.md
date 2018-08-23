---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 559680b9ca4ea5be85718d8f9692df93f77b0edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585753"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスのサービス プロバイダーを使用します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |プロバイダー管理オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IProviderAdmin  <br/> |
|ポインターの型。  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](iprovideradmin-getlasterror.md) <br/> |プロバイダーの管理オブジェクトに発生した前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |メッセージ サービスのプロバイダーのテーブル、メッセージ サービスのサービス プロバイダーの一覧へのアクセスを提供します。  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |メッセージ サービスにサービス プロバイダーを追加します。  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |メッセージ サービスからサービス プロバイダーを削除します。  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |現在のプロファイルからプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、 [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)メソッドを呼び出すことによって**IProviderAdmin**インターフェイスにポインターを取得することができます。メッセージ サービスのエントリ ポイント関数が呼び出されたときに、サービス プロバイダーは、 **IProviderAdmin**ポインターに渡されます。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

