---
title: MAPI でのメモリを管理します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c30aa631e70f8f4be52c2fd42dd6bfad900f379e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566160"
---
# <a name="managing-memory-in-mapi"></a>MAPI でのメモリを管理します。

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
方法とタイミングを割り当てるし、メモリを解放するのには、MAPI を使用するプログラミングの重要な部分です。 MAPI には、関数とマクロの両方を一貫した方法でメモリを管理するために、クライアントまたはサービス プロバイダーを使用できますが用意されています。 3 つの関数は次のとおりです。
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
クライアントとサービス ・ プロバイダーの問題、これらの関数を使用する場合の「所有者」-をリリースする方法を知っているが、-特定のメモリ ブロックを削除します。 サービス プロバイダーのメソッドを呼び出すクライアントは、任意のサイズの戻り値を保持するのに十分な大きさのバッファーを渡す必要がありますありません。 サービス プロバイダーは、 **MAPIAllocateBuffer**を使用しているメモリの適切な量を割り当てることが単にし、必要に応じて、 **MAPIAllocateMore**、およびクライアントが後で元の**MAPIFreeBuffer**サービスに関係なくを使用してはプロバイダーです。 
  
構造体または特定のサイズの構造体の配列を割り当てるメモリのマクロを使用します。 クライアントとサービス ・ プロバイダーする必要がありますこれらのマクロを使用してではなく手動でメモリを割り当てます。 などの場合は、クライアントは、名前解決の 3 つのエントリを持つ受信者リストの処理を実行する必要がある、 **SizedADRLIST**マクロ使えますの正しい数を**IAddrBook::ResolveName**に渡すための**ADRLIST**構造体を作成するには**ADRENTRY**メンバー。 すべてのメモリ ・ マクロは、MAPIDEFS で定義されます。H ヘッダー ファイルです。 これらのマクロは次のとおりです。 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI には、メモリ管理に[IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx)の COM インターフェイスの使用もサポートしています。 サービス プロバイダーは、 **IMalloc**インターフェイス ポインター式によって与えられます MAPI の初期化時と、 [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md)関数を 1 つを取得することもできます。 **IMalloc**メソッドを使用して MAPI の関数でメモリを管理するために主な利点は COM メソッドを使用して既存のバッファーを再割り当てすることです。 MAPI メモリ関数は、再割り当てをサポートしていません。 
  

