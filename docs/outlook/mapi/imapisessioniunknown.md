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
  
MAPI ログオン セッションに関連付けられているオブジェクトを管理します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|次のユーザーによって公開されます。  <br/> |セッション オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションと MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPISession  <br/> |
|ポインターの種類:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |前のセッション エラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |セッション プロファイル内のすべてのメッセージ ストアに関する情報を含むメッセージ ストア テーブルへのアクセスを提供します。  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |メッセージ ストアを開き、さらにアクセスする [IMsgStore ポインター](imsgstoreimapiprop.md) を返します。  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |MAPI 統合アドレス帳を開き [、IAddrBook](iaddrbookimapiprop.md) ポインターを返してさらにアクセスします。  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |セッション内のすべての MAPI リソースに関する情報を含むテーブルである状態テーブルへのアクセスを提供します。  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |オブジェクトを開き、さらにアクセスするインターフェイス ポインターを返します。  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。  <br/> |
|[アドバイス](imapisession-advise.md) <br/> |セッションに影響を与える指定されたイベントの通知を受信するために登録します。  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Advise メソッドの呼び出しで以前に設定された通知の送信を **キャンセル** します。  <br/> |
|**MessageOptions** <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |非推奨。 セッション内のすべてのトランスポート プロバイダーが処理できるアドレスの種類を返します。  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |セッションのプライマリ ID を提供するオブジェクトのエントリ識別子を返します。  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |MAPI セッションを終了します。  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |セッションの既定のメッセージ ストアとしてメッセージ ストアを確立します。  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |メッセージ サービスを [変更する IMsgServiceAdmin](imsgserviceadminiunknown.md) ポインターを返します。  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |フォームを表示します。  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |**ShowForm** メソッドがメッセージにアクセスするために使用する数値トークンを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

