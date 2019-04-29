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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431079"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーのリソースにアクセスします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|公開者:  <br/> |アドレス帳のログオンオブジェクト  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IABLogon  <br/> |
|ポインターの種類:  <br/> |lpablogon  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |以前のアドレス帳プロバイダーエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |ログオフプロセスを開始します。  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |コンテナー、メッセージングユーザー、または配布リストを開き、インターフェイス実装へのポインターを返して、さらにアクセスできるようにします。  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。  <br/> |
|[助言](iablogon-advise.md) <br/> |発信者が、コンテナー、メッセージングユーザー、または配布リストに影響を与える指定されたイベントの通知を受信するように登録します。  <br/> |
|[アドバイズ](iablogon-unadvise.md) <br/> |**アドバイズ**メソッドへの呼び出しで以前に設定された通知をキャンセルします。  <br/> |
|[openstatusentry](iablogon-openstatusentry.md) <br/> |プロバイダーの状態オブジェクトを開きます。  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |ホストアドレス帳プロバイダーに存在するデータを持つ受信者エントリを開きます。  <br/> |
|[getoneofftable](iablogon-getoneofftable.md) <br/> |送信メッセージの受信者リストに追加する受信者を作成するための、1回限りのテンプレートのテーブルを返します。  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |メッセージングシステムで後で使用するために、受信者リストを準備します。  <br/> |
   
## <a name="remarks"></a>注釈

**IABLogon**インターフェイスのメソッドに関する一般的な情報については、「[サービスプロバイダーログオンの実装](implementing-service-provider-logon.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

