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
ms.openlocfilehash: aba61d4acf7c1f9a5d91fa15f1ca6b16f173bcb2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309710"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル内のメッセージサービスの変更を行います。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|公開者:  <br/> |メッセージサービスの管理オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMsgServiceAdmin  <br/> |
|ポインターの種類:  <br/> |lpserviceadmin  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |メッセージサービス管理オブジェクトによって生成された最後のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[getmsgservicetable](imsgserviceadmin-getmsgservicetable.md) <br/> |メッセージサービステーブル (プロファイル内のメッセージサービスのリスト) へのアクセスを提供します。  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |現在のプロファイルにメッセージサービスを追加します。  <br/> <br/>**メモ**: このメソッドは推奨されていません。 代わりに[IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を使用します。           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |メッセージサービスをプロファイルから削除します。  <br/> |
|[copymsgservice](imsgserviceadmin-copymsgservice.md) <br/> |メッセージサービスをプロファイルにコピーします。  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |現在は廃止されています。 メッセージサービスに新しい名前を割り当てます。  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |メッセージサービスを再構成します。  <br/> |
|[openプロファイル '](imsgserviceadmin-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。  <br/> |
|[msgservicetransportorder](imsgserviceadmin-msgservicetransportorder.md) <br/> |メッセージを配信するためにトランスポートプロバイダーが呼び出される順序を設定します。  <br/> |
|[adminproviders](imsgserviceadmin-adminproviders.md) <br/> |プロバイダー管理オブジェクトへのアクセスを提供するポインターを返します。  <br/> |
|[setprimaryidentity](imsgserviceadmin-setprimaryidentity.md) <br/> |メッセージサービスがプロファイルのプライマリ id のサプライヤーであることを指定します。  <br/> |
|[getprovidertable](imsgserviceadmin-getprovidertable.md) <br/> |プロバイダーテーブルへのアクセスを提供します。これは、プロファイル内のサービスプロバイダーの一覧です。  <br/> |
   
## <a name="remarks"></a>解説

実装では、次の2つの方法で**IMsgServiceAdmin**インターフェイスへのポインターを取得できます。これには、 [imapisession:: adminservices](imapisession-adminservices.md)メソッドを呼び出すか、 [IProfAdmin:: adminservices](iprofadmin-adminservices.md)メソッドを呼び出します。 主にプロファイルの構成を考慮しているクライアントの場合は、 **IProfAdmin:: adminservices**を使用することをお勧めします。この方法では、 **IMsgServiceAdmin**インターフェイスを取得することをお勧めします。 クライアントでアクティブなプロファイルを変更する機能が必要な場合は、 **IMsgServiceAdmin**ポインターを取得するために**imapisession:: adminservices**を呼び出す必要があります。 MAPI では、使用中のプロファイルを削除することはできませんが、クライアントがプロファイル内のすべてのメッセージサービスを削除できないようにするためのセーフガードはありません。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

