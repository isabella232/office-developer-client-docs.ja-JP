---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 784430f1286c9a017337a0fae4b269757a56a3e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800368"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**適用対象**: Outlook 
  
アドレス帳プロバイダー内のリソースをアクセスします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって公開されます。  <br/> |アドレス帳ログオン オブジェクト  <br/> |
|によって実装されます。  <br/> |アドレス帳プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI  <br/> |
|インターフェイスの識別子。  <br/> |IID_IABLogon  <br/> |
|ポインターの型。  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](iablogon-getlasterror.md) <br/> |以前のアドレス帳プロバイダーのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |ログオフ処理を開始します。  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |コンテナー、ユーザー、または配布リストにメッセージを開き、さらにアクセスを提供するインターフェイスの実装にポインターを返します。  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。  <br/> |
|[アドバイス](iablogon-advise.md) <br/> |コンテナー、ユーザー、または配布リストをメッセージに影響を与える特定のイベントの通知を受け取る呼び出し元を登録します。  <br/> |
|[アドバイズ中止します。](iablogon-unadvise.md) <br/> |**アドバイズ**メソッドへの呼び出しで以前設定された通知をキャンセルします。  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |プロバイダーの状態のオブジェクトを開きます。  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |ホストのアドレス帳プロバイダーに存在するデータが含まれている受信者のエントリが表示されます。  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |送信メッセージの受信者の一覧に追加する受信者を作成するための 1 回限りのテンプレートのテーブルを返します。  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |メッセージング システムによって後で使用できる受信者のリストを準備します。  <br/> |
   
## <a name="remarks"></a>注釈

**IABLogon**インターフェイスのメソッドの詳細については、[実装するサービス プロバイダーへのログオン](implementing-service-provider-logon.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

