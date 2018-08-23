---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cf275c66a60ed977c442b468b7c9951325db5120
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593516"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイル内のメッセージ サービスを変更します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |MapiX.h  <br/> |
|によって公開されます。  <br/> |メッセージ サービス管理オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMsgServiceAdmin  <br/> |
|ポインターの型。  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](imsgserviceadmin-getlasterror.md) <br/> |メッセージ サービス管理オブジェクトによって生成された最後のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |メッセージ サービス テーブルで、[プロファイルのメッセージ サービスの一覧へのアクセスを提供します。  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |メッセージ サービスは、現在のプロファイルに追加します。  <br/> <br/>**注**: このメソッドは推奨されません。 [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を使用してください。           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |メッセージ サービスをプロファイルから削除します。  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |メッセージ サービスをプロファイルにコピーします。  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |現在は廃止されています。 メッセージ サービスに新しい名前が割り当てられます。  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |メッセージ サービスを再構成します。  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |どのトランスポートにメッセージを配信するプロバイダーの呼び出し順序を設定します。  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |プロバイダー管理オブジェクトへのアクセスを提供するポインターを返します。  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |メッセージ サービス プロファイルのプライマリ id のサプライヤーになることを指定します。  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |プロバイダー テーブル、プロファイル内のサービス プロバイダーの一覧へのアクセスを提供します。  <br/> |
   
## <a name="remarks"></a>注釈

実装は 2 つの方法に**IMsgServiceAdmin**インターフェイスにポインターを取得することができます: [IMAPISession::AdminServices](imapisession-adminservices.md)メソッドを呼び出すことによって、または[IProfAdmin::AdminServices](iprofadmin-adminservices.md)メソッドを呼び出しています。 MAPI セッション プロバイダーのログ出力しないために、クライアント プロファイルの構成とパフォーマンスに着目は、 **IProfAdmin::AdminServices** 、 **IMsgServiceAdmin**のインターフェイスを取得する優先方法です。 クライアントは、アクティブなプロファイルを変更する機能を必要とする場合、 **IMsgServiceAdmin**のポインターを取得する**IMAPISession::AdminServices**を呼び出す必要があります。 MAPI プロファイルを削除するのには使用されていることはできません、がないクライアントのプロファイルのすべてのメッセージ サービスを削除することを防ぐための安全対策に注意します。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

