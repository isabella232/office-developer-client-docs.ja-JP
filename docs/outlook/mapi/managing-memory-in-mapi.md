---
title: MAPI でのメモリの管理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298097"
---
# <a name="managing-memory-in-mapi"></a>MAPI でのメモリの管理

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メモリの割り当てと解放の方法とタイミングを知ることは、MAPI を使用したプログラミングの重要な部分です。 MAPI には、クライアントまたはサービスプロバイダーが一貫した方法でメモリを管理するために使用できる関数とマクロの両方が用意されています。 3つの関数は次のとおりです。
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
クライアントおよびサービスプロバイダーがこれらの機能を使用する場合、誰がどのようなメモリブロックを解放するかを知ることができます。 サービスプロバイダメソッドを呼び出すクライアントは、任意のサイズの戻り値を保持するために十分に大きいバッファーを通過する必要はありません。 サービスプロバイダーは単に、 **MAPIAllocateBuffer**を使用して適切な量のメモリを割り当てることができ、必要に応じて**MAPIAllocateMore**、クライアントは後で**MAPIFreeBuffer**を使用して、サービスに依存することなく、そのメモリを解放できます。供給. 
  
メモリマクロは、構造体または特定のサイズの構造の配列を割り当てるために使用されます。 クライアントおよびサービスプロバイダーは、メモリを手動で割り当てる代わりに、これらのマクロを使用する必要があります。 たとえば、クライアントが3つのエントリを持つ受信者リストで名前解決処理を実行する必要がある場合、 **sizedadrlist**マクロを使用して、 **IAddrBook:: ResolveName**に渡される**adrlist**構造を作成し、正しい数の**adrentry**のメンバー。 mapidefs.h では、すべてのメモリマクロが定義されています。H ヘッダーファイル。 これらのマクロは次のとおりです。 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI では、メモリ管理用の COM インターフェイス[imalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx)の使用もサポートしています。 サービスプロバイダーには、初期化時に MAPI によって**imalloc**インターフェイスポインターが与えられ、 [mapigetdefaultmalloc](mapigetdefaultmalloc.md)関数を使用して取得することもできます。 MAPI 関数でメモリを管理するために**imalloc**メソッドを使用する主な利点は、COM メソッドを使用して既存のバッファーを再割り当てできることです。 MAPI メモリ関数は再割り当てをサポートしていません。 
  

