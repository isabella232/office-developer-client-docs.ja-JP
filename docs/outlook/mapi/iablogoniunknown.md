---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d2f7bfd8c1bcc15cc12e4ab6efd26b0591f11b27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614025"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーのリソースにアクセスします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|次のユーザーによって公開されます。  <br/> |アドレス帳ログオン オブジェクト  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IABLogon  <br/> |
|ポインターの種類:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |以前のアドレス [帳プロバイダー エラー](mapierror.md) に関する情報を含む MAPIERROR 構造体を返します。  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |ログオフ プロセスを開始します。  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |コンテナー、メッセージング ユーザー、または配布リストを開き、インターフェイス実装へのポインターを返して、さらにアクセスを提供します。  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。  <br/> |
|[アドバイス](iablogon-advise.md) <br/> |コンテナー、メッセージング ユーザー、または配布リストに影響を与える指定されたイベントの通知を受け取る呼び出し元を登録します。  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Advise メソッドの呼び出しで以前に設定された通知を **取り消** します。  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |プロバイダーの状態オブジェクトを開きます。  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |ホスト アドレス帳プロバイダーに存在するデータを含む受信者エントリを開きます。  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |送信メッセージの受信者リストに追加する受信者を作成するための一時テンプレートのテーブルを返します。  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |メッセージング システムで後で使用する受信者リストを準備します。  <br/> |
   
## <a name="remarks"></a>注釈

**IABLogon** インターフェイスのメソッドの一般的な情報については、「Service Provider Logon の実装 [」を参照してください](implementing-service-provider-logon.md)。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

