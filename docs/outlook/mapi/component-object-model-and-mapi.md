---
title: コンポーネント オブジェクト モデルと MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334469"
---
# <a name="component-object-model-and-mapi"></a>コンポーネント オブジェクト モデルと MAPI

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Windows SDK ドキュメントには、コンポーネントオブジェクトモデル (COM) に準拠するオブジェクトを実装するための規則についての包括的な説明が含まれています。 これらのルールは、次の操作を実行する方法に対応しています。
  
- インターフェイスとオブジェクトを設計します。
    
- [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスを実装します。 
    
- メモリを管理します。
    
- 参照カウントを処理します。
    
- アパートメントスレッドオブジェクトを実装します。
    
すべての mapi オブジェクトは、 [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)から継承するインターフェイスを実装するため、com ベースであると見なされますが、一部の状況では、標準的な com ルールによって異なります。 この偏差により、開発者は実装をより柔軟にすることができます。 たとえば、すべての COM インターフェイスと同様に、MAPI インターフェイスは、実装側と呼び出し元との間の契約を記述します。 インターフェイスを作成して発行すると、その定義は変更できなくなります。 MAPI はこの説明から逸脱しませんが、説明は少し relaxes ます。 実装者は、特定のメソッドを実装しないことを選択でき、次のいずれかのエラー値を呼び出し元に返します。 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
次の表では、標準 COM ルールのその他の相違点について説明します。
  
|**COM プログラミングルール**|**MAPI のバリエーション**|
|:-----|:-----|
|インターフェイスメソッドのすべての文字列パラメーターは Unicode にする必要があります。  <br/> |MAPI インターフェイスは、Unicode または ANSI 文字列パラメーターのいずれかを許可するように定義されています。 文字列パラメーターを持つ多くのメソッドに**ulflags**パラメーターも指定されています。文字列パラメータの幅は、 **ulflags**の MAPI_UNICODE フラグの値で示されます。 一部の MAPI インターフェイスは、Unicode をサポートしておらず、MAPI_UNICODE フラグが設定されている場合は MAPI_E_BAD_CHARWIDTH を返します。  <br/> |
|すべてのインターフェイスメソッドには、戻り値の型が HRESULT である必要があります。  <br/> |MAPI には、HRESULT でない値: [IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)を返すメソッドが少なくとも1つあります。  <br/> |
|呼び出し元と実装者は、標準の COM タスク allocators を使用して、インターフェイスパラメーターのメモリを割り当てて解放する必要があります。  <br/> |すべての MAPI メソッドは、リンクされた allocators [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)を使用して、インターフェイスパラメーターのメモリを管理します。 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)など、OLE によって定義されたインターフェイスのすべての MAPI 実装は、標準の COM タスク allocators を使用します。  <br/> |
|メソッドが失敗した場合は、すべての out ポインターパラメーターを明示的に NULL に設定する必要があります。  <br/> |MAPI インターフェイスでは、out ポインターパラメーターを NULL に設定するか、またはメソッドが失敗した場合は変更しないままにする必要があります。 OLE によって定義されたインターフェイスのすべての MAPI 実装は、失敗時にパラメーターを NULL に明示的に設定します。  <br/> |
|可能な限り、集約可能なオブジェクトを実装します。  <br/> |MAPI インターフェイスは集約できません。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI のオブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

