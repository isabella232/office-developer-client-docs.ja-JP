---
title: imapisession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413382"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI ログオンセッションに関連付けられているオブジェクトを管理します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|公開者:  <br/> |Session オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションと MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPISession  <br/> |
|ポインターの種類:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |前のセッションエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[getmsgstorestable](imapisession-getmsgstorestable.md) <br/> |セッションプロファイル内のすべてのメッセージストアに関する情報を含むメッセージストアテーブルへのアクセスを提供します。  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |メッセージストアを開き、さらにアクセスするための[IMsgStore](imsgstoreimapiprop.md)ポインターを返します。  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |MAPI 統合アドレス帳を開き、さらにアクセスするために[IAddrBook](iaddrbookimapiprop.md)ポインターを返します。  <br/> |
|[openプロファイル '](imapisession-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。  <br/> |
|[getstatustable](imapisession-getstatustable.md) <br/> |状態テーブル (セッション内のすべての MAPI リソースに関する情報を含むテーブル) へのアクセスを提供します。  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |オブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。  <br/> |
|[助言](imapisession-advise.md) <br/> |セッションに影響を与える指定したイベントの通知を受信するように登録します。  <br/> |
|[アドバイズ](imapisession-unadvise.md) <br/> |**アドバイズ**メソッドへの呼び出しを使用して、以前に設定した通知の送信をキャンセルします。  <br/> |
|**messageoptions** <br/> | *サポートされていないか文書化されていません。*  <br/> |
|**querydefaultmessageopt** <br/> | *サポートされていないか文書化されていません。*  <br/> |
|[enumadrtypes](imapisession-enumadrtypes.md) <br/> |現在は廃止されています。 セッション内のすべてのトランスポートプロバイダーで処理できるアドレスの種類を返します。  <br/> |
|[queryidentity](imapisession-queryidentity.md) <br/> |セッションのプライマリ id を提供するオブジェクトのエントリ id を返します。  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |MAPI セッションを終了します。  <br/> |
|[setdefaultstore](imapisession-setdefaultstore.md) <br/> |セッションの既定のメッセージストアとしてメッセージストアを確立します。  <br/> |
|[adminservices](imapisession-adminservices.md) <br/> |メッセージサービスに変更を加えるための[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。  <br/> |
|[showform](imapisession-showform.md) <br/> |フォームを表示します。  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |**showform**メソッドがメッセージにアクセスするために使用する数値トークンを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

