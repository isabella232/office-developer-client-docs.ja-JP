---
title: MAPI でのメモリの管理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298097"
---
# <a name="managing-memory-in-mapi"></a>MAPI でのメモリの管理

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メモリを割り当て、解放する方法と時間を知ることは、MAPI を使用したプログラミングの重要な部分です。 MAPI には、クライアントまたはサービス プロバイダーが一貫した方法でメモリを管理するために使用できる関数とマクロの両方が提供されています。 3 つの関数は次のとおりです。
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
クライアントとサービス プロバイダーがこれらの関数を使用すると、特定のメモリ ブロックを解放する方法を知っているユーザー (つまり、所有するユーザー) の問題が解消されます。 サービス プロバイダー メソッドを呼び出すクライアントは、任意のサイズの戻り値を保持するのに十分な大きさのバッファーを渡す必要があります。 サービス プロバイダーは **、MAPIAllocateBuffer** を使用して適切な量のメモリを割り当て、必要に応じて **MAPIAllocateMore** を割り当て、クライアントは、サービス プロバイダーとは別に **、MAPIFreeBuffer** を使用して後で解放できます。 
  
メモリ マクロは、特定のサイズの構造体または構造体の配列を割り当てるのに使用されます。 クライアントとサービス プロバイダーは、メモリを手動で割り当てるのではなく、これらのマクロを使用する必要があります。 たとえば、クライアントが 3 つのエントリを含む受信者リストで名前解決処理を実行する必要がある場合 **、SizedADRLIST** マクロを使用して、正しい数の **ADRENTRY** メンバーを持つ **IAddrBook::ResolveName** に渡す **ADRLIST** 構造を作成できます。 すべてのメモリ マクロは MAPIDEFS で定義されています。H ヘッダー ファイル。 これらのマクロは次のとおりです。 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI は、メモリ管理のための COM インターフェイス [IMalloc の](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) 使用もサポートしています。 サービス プロバイダーには、初期化時に MAPI によって **IMalloc** インターフェイス ポインターが与え [、MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) 関数を介して取得することもできます。 **IMalloc** メソッドを使用して MAPI 関数を使用してメモリを管理する主な利点は、COM メソッドを使用すると、既存のバッファーを再割り当てできるという利点があります。 MAPI メモリ関数は、割り当て解除をサポートしていない。 
  

