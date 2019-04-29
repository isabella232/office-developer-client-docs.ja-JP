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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412864"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーオブジェクトを使用して、メッセージストアプロバイダーへのアクセスを提供します。 このメッセージストアプロバイダオブジェクトは、メッセージストアプロバイダーの[msproviderinit](msproviderinit.md) entry point 関数によってプロバイダログオンで返されます。 メッセージストアプロバイダーオブジェクトは、主にクライアントアプリケーションと MAPI スプーラーによって、メッセージストアを開くために使用されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|公開者:  <br/> |メッセージ ストア プロバイダーのオブジェクト  <br/> |
|実装元:  <br/> |メッセージストアプロバイダー  <br/> |
|呼び出し元:  <br/> |mapi および mapi スプーラー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMSProvider  <br/> |
|ポインターの種類:  <br/> |lpmsprovider  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[シャットダウン](imsprovider-shutdown.md) <br/> |メッセージストアプロバイダーを整然と閉じます。  <br/> |
|[Logon](imsprovider-logon.md) <br/> |メッセージストアプロバイダーの1つのインスタンスに MAPI を記録します。  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |MAPI スプーラーをメッセージストアに記録します。  <br/> |
|[comparestoreids](imsprovider-comparestoreids.md) <br/> |2つのメッセージストアエントリ識別子を比較して、同じ store オブジェクトを参照しているかどうかを判断します。  <br/> |
   
## <a name="remarks"></a>注釈

MAPI では、ストアプロバイダーによって開かれるメッセージストアの数に関係なく、セッションごとに1つのメッセージストアプロバイダオブジェクトが使用されます。 2番目の mapi セッションが開いているストアにログオンすると、mapi は**msproviderinit**をもう一度呼び出して、そのセッションで使用する新しいメッセージストアプロバイダオブジェクトを作成します。 
  
メッセージストアプロバイダオブジェクトには、正しく動作するために次のものが含まれている必要があります。
  
- このプロバイダーオブジェクトを使用して開かれたすべてのストアが使用する_lpmalloc_メモリ割り当てルーチンポインター。 
    
- [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)のメモリ割り当て関数への_lpfAllocateBuffer_、_ lpfAllocateMore _、および_lpfFreeBuffer_ルーチンポインター。 
    
- このプロバイダオブジェクトを使用して開かれているが、まだ閉じていないすべてのストアのリンクリスト。
    
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

