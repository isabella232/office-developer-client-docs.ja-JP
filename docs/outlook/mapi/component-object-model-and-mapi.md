---
title: コンポーネント オブジェクト モデルおよび MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cf687a7bfadb0981ca3440c2f81bc5de8f910924
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799820"
---
# <a name="component-object-model-and-mapi"></a>コンポーネント オブジェクト モデルおよび MAPI

  
  
**適用されます**: Outlook 
  
Windows SDK ドキュメントには、コンポーネント オブジェクト モデル (COM) に準拠しているオブジェクトを実装するための規則の包括的な説明が含まれています。 これらの規則は、以下を実行する方法を対処します。
  
- インターフェイスとオブジェクトを設計します。
    
- [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx)インターフェイスを実装します。 
    
- メモリを管理します。
    
- 参照カウントを処理します。
    
- アパートメント スレッド オブジェクトを実装します。
    
すべての MAPI オブジェクトと見なされます com [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx)から継承するインターフェイスを実装するため、MAPI は、状況によっては標準の COM の規則からの逸脱します。 この偏差から、開発者は、実装でより柔軟にすることができます。 などの任意の COM インターフェイスと同様に、MAPI インターフェイスでは、作成者と呼び出し元のコントラクトについて説明します。 インタ フェースが作成され、公開、その定義はことはできず、変更されません。 この説明では、MAPI が外れていないが、説明を多少緩和します。 実装では特定のメソッドを実装するのにはエラー値は次のいずれかを呼び出し元に返すことができます。 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
標準の COM の規則からの偏差は、次の表に説明します。
  
|**COM プログラミングの規則**|**MAPI のバリエーション**|
|:-----|:-----|
|インターフェイスのメソッド内のすべての文字列パラメーターには、Unicode をする必要があります。  <br/> |MAPI インターフェイスは、Unicode または ANSI のいずれかの文字列パラメーターを許可するように定義されます。 文字列パラメーターをとるメソッドの多くもパラメーターを持つ、 **ulFlags**です。**ulFlags**に MAPI_UNICODE フラグの値の文字列パラメーターの幅が表示されます。 一部の MAPI インターフェイスをサポートしない Unicode MAPI_UNICODE フラグが設定されている場合は、MAPI_E_BAD_CHARWIDTH を返します。  <br/> |
|すべてのインターフェイス メソッドは、HRESULT の戻り値の型が必要です。  <br/> |MAPI 以外の HRESULT 値を返すには、少なくとも 1 つのメソッドを持つ: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)。  <br/> |
|呼び出し元および実装する必要があります解放し、メモリ インタ フェースのパラメーターの標準的な COM タスク アロケーターを使用しています。  <br/> |MAPI のすべてのメソッドは、インターフェイスのパラメーター用のメモリを管理するために[MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)は、リンクされたアロケーターを使用します。 [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)など、OLE によって定義されたインターフェイスのすべての MAPI 実装では、標準的な COM タスク アロケーターを使用します。  <br/> |
|すべてのポインター パラメーターする必要があります明示的に設定する NULL にメソッドが失敗したとき。  <br/> |MAPI インターフェイスでは、ポインター パラメーターを NULL に設定または変更しないままメソッドを配置するかを失敗する必要があります。 OLE によって明示的に定義されているインタ フェースのすべての MAPI 実装では、失敗した場合に null パラメーターを設定します。  <br/> |
|可能な限り、集約可能オブジェクトを実装します。  <br/> |MAPI インターフェイスは、集約可能ではありません。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)
