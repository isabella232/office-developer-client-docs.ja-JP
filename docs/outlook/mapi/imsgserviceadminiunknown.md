---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e4c66a4a06cbfb3907053aead043c03dcb0cfe60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579867"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル内のメッセージ サービスに変更を加えます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |MapiX.h  <br/> |
|次のユーザーによって公開されます。  <br/> |メッセージ サービス管理オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMsgServiceAdmin  <br/> |
|ポインターの種類:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |メッセージ サービス管理オブジェクトによって生成された最後のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |プロファイル内のメッセージ サービスの一覧であるメッセージ サービス テーブルへのアクセスを提供します。  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |現在のプロファイルにメッセージ サービスを追加します。  <br/> <br/>**メモ**: このメソッドは非推奨です。 代 [わりに、IMsgServiceAdmin2::CreateMsgServiceEx を](imsgserviceadmin2-createmsgserviceex.md) 使用します。           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |プロファイルからメッセージ サービスを削除します。  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |メッセージ サービスをプロファイルにコピーします。  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |非推奨。 メッセージ サービスに新しい名前を割り当てる。  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |メッセージ サービスを再構成します。  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |メッセージを配信するためにトランスポート プロバイダーが呼び出される順序を設定します。  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |プロバイダー管理オブジェクトへのアクセスを提供するポインターを返します。  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |メッセージ サービスをプロファイルのプライマリ ID のサプライヤーに指定します。  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |プロファイル内のサービス プロバイダーの一覧であるプロバイダー テーブルへのアクセスを提供します。  <br/> |
   
## <a name="remarks"></a>注釈

実装では [、IMAPISession::AdminServices](imapisession-adminservices.md)メソッドを呼び出すことによって、[または IProfAdmin::AdminServices](iprofadmin-adminservices.md)メソッドを呼び出すことによって **、IMsgServiceAdmin** インターフェイスへのポインターを取得できます。 主にプロファイル構成に関するクライアントの場合 **、IProfAdmin::AdminServices** は、プロバイダーを MAPI セッションにログオンしないので **、IMsgServiceAdmin** インターフェイスを取得するための推奨方法です。 クライアントでアクティブ なプロファイルを変更する機能が必要な場合は **、IMsgServiceAdmin** ポインターを取得するために **IMAPISession::AdminServices** を呼び出す必要があります。 MAPI では、使用されているプロファイルの削除は許可されませんが、クライアントがプロファイル内のすべてのメッセージ サービスを削除しないセーフガードはありません。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

