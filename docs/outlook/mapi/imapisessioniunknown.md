---
title: IMAPISession IUnknown
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 163bce38d665a8566fd703420ff1f7b2f44f7c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571809"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI ログオン セッションに関連付けられているオブジェクトを管理します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって公開されます。  <br/> |セッション オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションと MAPI  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPISession  <br/> |
|ポインターの型。  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](imapisession-getlasterror.md) <br/> |前のセッションのエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |セッション ・ プロファイル内のすべてのメッセージ ・ ストアに関する情報を含むメッセージ ストアのテーブルへのアクセスを提供します。  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |メッセージ ストアを開き、さらにアクセスするための[IMsgStore](imsgstoreimapiprop.md)ポインターを返します。  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |さらにアクセスするための[IAddrBook](iaddrbookimapiprop.md)ポインターを返す MAPI 統合アドレス帳を開きます。  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |ステータス テーブル、セッション内のすべての MAPI リソースに関する情報が含まれているテーブルへのアクセスを提供します。  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |オブジェクトを開き、さらにアクセスするためのインターフェイス ポインターを返します。  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。  <br/> |
|[アドバイス](imapisession-advise.md) <br/> |セッションに影響を与える特定のイベントの通知を受け取ることを登録します。  <br/> |
|[アドバイズ中止します。](imapisession-unadvise.md) <br/> |**アドバイズ**メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。  <br/> |
|**オプション** <br/> | *いないサポートまたは文書化されています。*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *いないサポートまたは文書化されています。*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |現在は廃止されています。 セッション内のすべてのトランスポート プロバイダーによって処理可能なアドレスの種類を返します。  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |セッションのプライマリ id を提供するオブジェクトのエントリ id を返します。  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |MAPI セッションを終了します。  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |セッションの既定のメッセージ ストアとしてのメッセージ ・ ストアを確立します。  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |メッセージ サービスを変更する場合、 [IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |フォームが表示されます。  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |**ShowForm**メソッドを使用してメッセージにアクセスする数値のトークンを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

