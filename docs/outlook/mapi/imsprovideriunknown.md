---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d24f2c0697a3aad951625837fa3e56cf6fb9ccd3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575659"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダー オブジェクトを介してメッセージ ストア プロバイダーへのアクセスを提供します。 このメッセージ ストア プロバイダー オブジェクトは、メッセージ ストア プロバイダーの [MSProviderInit](msproviderinit.md) エントリ ポイント関数によってプロバイダー ログオン時に返されます。 メッセージ ストア プロバイダー オブジェクトは、主にクライアント アプリケーションと MAPI スプーラーによってメッセージ ストアを開く目的で使用されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|次のユーザーによって公開されます。  <br/> |メッセージ ストア プロバイダーのオブジェクト  <br/> |
|実装元:  <br/> |メッセージ ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI と MAPI スプーラー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMSProvider  <br/> |
|ポインターの種類:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[シャットダウン](imsprovider-shutdown.md) <br/> |メッセージ ストア プロバイダーを順番に閉じます。  <br/> |
|[Logon](imsprovider-logon.md) <br/> |メッセージ ストア プロバイダーの 1 つのインスタンスに MAPI をログオンします。  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |MAPI スプーラーをメッセージ ストアにログに記録します。  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |2 つのメッセージ ストア エントリ識別子を比較して、同じストア オブジェクトを参照するかどうかを判断します。  <br/> |
   
## <a name="remarks"></a>注釈

MAPI は、ストア プロバイダーによって開くメッセージ ストアの数に関係なく、セッションごとに 1 つのメッセージ ストア プロバイダー オブジェクトを使用します。 2 つ目の MAPI セッションが開いているストアにログオンすると、MAPI は **MSProviderInit** を 2 回目に呼び出して、そのセッションで使用する新しいメッセージ ストア プロバイダー オブジェクトを作成します。 
  
正しく動作するには、メッセージ ストア プロバイダー オブジェクトに次の情報が含まれている必要があります。
  
- この  _プロバイダー オブジェクトを使用_ して開かれたすべてのストアで使用する lpMalloc メモリ割り当てルーチン ポインター。 
    
- _lpfAllocateBuffer_、_ lpfAllocateMore _、_および lpfFreeBuffer_ ルーチン ポインターから [MAPIAllocateBuffer、MAPIAllocateMore、MAPIFreeBuffer](mapiallocatebuffer.md)メモリ割り当て関数を取得します。 [](mapiallocatemore.md) [](mapifreebuffer.md) 
    
- このプロバイダー オブジェクトを使用して開き、まだ閉じていないすべてのストアのリンクリスト。
    
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

