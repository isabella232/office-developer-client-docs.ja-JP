---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c00e54d02ba494c94c9826eabe142e1bd3b9a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579628"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ストア プロバイダー オブジェクトを使用して、メッセージ ストア プロバイダーへのアクセスを提供します。 このメッセージ ストア プロバイダー オブジェクトは、メッセージ ストア プロバイダーの[MSProviderInit](msproviderinit.md)のエントリ ポイント関数がプロバイダーへのログオンに返されます。 メッセージ ストア プロバイダー オブジェクトは、メッセージ ストアを開くクライアント アプリケーションと MAPI スプーラーによって主に使用します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって公開されます。  <br/> |メッセージ ストア プロバイダー オブジェクト  <br/> |
|によって実装されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI および MAPI スプーラー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMSProvider  <br/> |
|ポインターの型。  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[シャットダウン](imsprovider-shutdown.md) <br/> |適切な順序で、メッセージ ストア プロバイダーを閉じます。  <br/> |
|[Logon](imsprovider-logon.md) <br/> |MAPI メッセージ ストア プロバイダーのインスタンスを 1 つにログに記録します。  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |メッセージ ストアに、MAPI スプーラーをログに記録します。  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |比較 2 つのメッセージが同じストア オブジェクトを参照しているかどうかを判断するのには、ストア エントリ id です。  <br/> |
   
## <a name="remarks"></a>注釈

MAPI セッションごとに 1 つのメッセージ ストア プロバイダー オブジェクトを使用して、メッセージの数に関係なく、ストアがストア プロバイダーによって開かれています。 2 つ目 MAPI セッションが開いているすべての店舗に場合、MAPI 呼び出し**MSProviderInit** 2 回目を使用するには、そのセッション用の新しいメッセージ ストア プロバイダー オブジェクトを作成します。 
  
メッセージ ストア プロバイダー オブジェクトは、正常に動作させるのには、次を含める必要があります。
  
- _LpMalloc_メモリ割り当てルーチンのポインターこのプロバイダー オブジェクトを使用して開かれたすべての店舗で使用するため。 
    
- _LpfAllocateBuffer_、_ lpfAllocateMore _ と_lpfFreeBuffer_ルーチンへのポインター、 [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)のメモリ割り当て関数。 
    
- このプロバイダー オブジェクトを使用して開かれ、閉じられていないすべてのストアのリンクのリストです。
    
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

