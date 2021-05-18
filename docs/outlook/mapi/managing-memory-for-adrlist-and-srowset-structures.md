---
title: ADRLIST および SRowSet 構造のためのメモリ管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407866"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>ADRLIST および SRowSet 構造体のメモリを管理する"

**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つの **MAPIAllocateBuffer** 呼び出しで可能な限りバッファーのすべてのメモリを割り当てる要件は、アドレス一覧または **ADRLIST**、および行セット、または **SRowSet** 構造体を使用する場合は適用されません。 
  
これら 2 つの構造は、メモリの割り当てと解放に関する標準ルールの例外です。 これらは複数のレベルの構造を含み、個々のメンバーを追加または削除するように設計されています。 したがって、各プロパティは個別の割り当てである必要があります。 

ほとんどの構造体が **MAPIFreeBuffer** への 1 回の呼び出しで解放される場合は **、ADRLIST** 構造体または **SRowSet** 構造体の各個々のエントリを **、MAPIFreeBuffer** への独自の呼び出しまたは **FreeProws** または **FreePadrlist** への 1 回の呼び出しで解放する必要があります。 詳細については [、「MAPIFreeBuffer](mapifreebuffer.md) [、ADRLIST、](adrlist.md)および [SRowSet」を参照してください](srowset.md)。 

**FreeProws と** **FreePadrlist は** 、これらのデータ構造の解放を簡略化するために MAPI によって提供される関数です。 詳細については [、「FreeProws and](freeprows.md) [FreePadrlist」を参照してください](freepadrlist.md)。 **FreePadrlist は****、ADRLIST** 構造体のメモリと、その構造体メンバーに関連付けられているすべてのメモリを解放します。**FreeProws は** **SRowSet 構造体でも同じことを** 行います。 
  
次の図は **、ADRLIST** データ構造のレイアウトを示しています。必要な個別のメモリ割り当てを示します。 灰色のボックスには、1 回の呼び出しで割り当ておよび解放できるメモリが表示されます。 
  
**ADRLIST メモリの割り当て**
  
![ADRLIST メモリ割り当て](media/amapi_52.gif "ADRLIST メモリ割り当て")
  
## <a name="see-also"></a>関連項目

- [MAPI でのメモリの管理](managing-memory-in-mapi.md)

