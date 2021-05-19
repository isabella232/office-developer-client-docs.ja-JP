---
title: コンポーネント オブジェクト モデルと MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334469"
---
# <a name="component-object-model-and-mapi"></a>コンポーネント オブジェクト モデルと MAPI

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
SDK Windowsドキュメントには、コンポーネント オブジェクト モデル (COM) に準拠するオブジェクトを実装するためのルールの包括的な説明が含まれています。 これらのルールは、次の方法に対処します。
  
- インターフェイスとオブジェクトを設計します。
    
- [IUnknown インターフェイスを実装](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)します。 
    
- メモリを管理します。
    
- 参照カウントを処理します。
    
- アパートメント スレッド オブジェクトを実装します。
    
すべての MAPI オブジェクトは [、IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)から継承するインターフェイスを実装するために COM ベースと見なされますが、MAPI は一部の状況では標準の COM ルールから離れる場合があります。 このずれにより、開発者は実装の柔軟性を高める可能性があります。 たとえば、MAPI インターフェイスは、任意の COM インターフェイスと同様に、実装者と呼び出し元の間のコントラクトについて説明します。 インターフェイスを作成して公開すると、その定義は変更できません。変更されません。 MAPI は、この説明から逸脱しないが、説明をややリラックスさせる。 実装者は、呼び出し元に次のいずれかのエラー値を返す、特定のメソッドを実装しない選択できます。 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
標準 COM ルールからのその他の偏差については、次の表で説明します。
  
|**COM プログラミング ルール**|**MAPI のバリエーション**|
|:-----|:-----|
|インターフェイス メソッドのすべての文字列パラメーターは Unicode である必要があります。  <br/> |MAPI インターフェイスは、Unicode または ANSI 文字列パラメーターのいずれかを許可するために定義されます。 文字列パラメーターを持つ多くのメソッドにも **ulFlags パラメーター** があります。文字列パラメーター の幅は **、ulFlags** の MAPI_UNICODEの値で示されます。 MAPI インターフェイスの中には、Unicode をサポートしていないものMAPI_E_BAD_CHARWIDTHフラグが設定MAPI_UNICODE返されます。  <br/> |
|すべてのインターフェイス メソッドには、HRESULT の戻り値の型が必要です。  <br/> |MAPI には、HRESULT 以外の値を返す少なくとも 1 つのメソッドがあります [。IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)です。  <br/> |
|呼び出し元と実装者は、標準の COM タスク アロケーターを使用して、インターフェイス パラメーターのメモリを割り当て、解放する必要があります。  <br/> |すべての MAPI メソッドは、リンクされたアロケーター MAPIAllocateBuffer、MAPIAllocateMore、MAPIFreeBuffer を使用して、インターフェイス パラメーターのメモリを管理します。 [](mapiallocatebuffer.md) [](mapiallocatemore.md) [](mapifreebuffer.md) [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)など、OLE によって定義されたインターフェイスのすべての MAPI 実装では、標準の COM タスク アロケーターを使用します。  <br/> |
|メソッドが失敗した場合は、すべてのアウト ポインター パラメーターを明示的に NULL に設定する必要があります。  <br/> |MAPI インターフェイスでは、メソッドが失敗した場合、ポインター パラメーターを NULL に設定するか、変更しないままにしてください。 OLE によって定義されたインターフェイスのすべての MAPI 実装は、エラー時にパラメーターを NULL に明示的に設定します。  <br/> |
|可能な限り、aggregatable オブジェクトを実装します。  <br/> |MAPI インターフェイスは、アグリガテーブルではありません。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

