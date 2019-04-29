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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437533"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスのサービスプロバイダーと連携します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |プロバイダー管理オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IProviderAdmin  <br/> |
|ポインターの種類:  <br/> |lpprovideradmin  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |プロバイダー管理オブジェクトに発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[getprovidertable](iprovideradmin-getprovidertable.md) <br/> |メッセージサービスのプロバイダーテーブルへのアクセスを提供します。これには、メッセージサービスのサービスプロバイダーの一覧が含まれます。  <br/> |
|[createprovider](iprovideradmin-createprovider.md) <br/> |メッセージサービスにサービスプロバイダーを追加します。  <br/> |
|[deleteprovider](iprovideradmin-deleteprovider.md) <br/> |メッセージサービスからサービスプロバイダーを削除します。  <br/> |
|[openプロファイル '](iprovideradmin-openprofilesection.md) <br/> |現在のプロファイルからプロファイルセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、 [IMsgServiceAdmin:: adminproviders](imsgserviceadmin-adminproviders.md)メソッドを呼び出して、 **IProviderAdmin**インターフェイスへのポインターを取得できます。サービスプロバイダーのメッセージサービスのエントリポイント関数が呼び出されると、 **IProviderAdmin**ポインターが渡されます。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

