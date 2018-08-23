---
title: ADRLIST と SRowSet 構造体のメモリを管理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ef20cf8460aa7d3d160208109e42b2de66658d54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589729"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>ADRLIST と SRowSet 構造体のメモリを管理するには」

**適用されます**: Outlook 2013 |Outlook 2016 
  
バッファーに割り当てるすべてのメモリを 1 つの**MAPIAllocateBuffer**呼び出しを可能な限り要件は、アドレス一覧、または**ADRLIST**、および行セット、または**SRowSet**、構造体を使用する場合に適用されません。 
  
これら 2 つの構造体は、割り当てとメモリを解放するための標準的な規則の例外です。 構造体の複数のレベルが含まれている、個々 のメンバーを追加または削除を有効にするように設計されています。 したがって、各プロパティは、個別の割り当てをする必要があります。 

独自の呼び出しを**MAPIFreeBuffer**または**FreeProws**または**のいずれか 1 回の呼び出しで解放する必要があります**MAPIFreeBuffer**、 **ADRLIST**または**SRowSet**構造体の個々 のエントリごとに 1 つの呼び出しのほとんどの構造体を解放する場所FreePadrlist**。 詳細については、 [MAPIFreeBuffer](mapifreebuffer.md)、 [ADRLIST](adrlist.md)、および[SRowSet](srowset.md)を参照してください。 

**FreeProws**と**FreePadrlist**は、これらのデータ構造体の解放を簡略化するため、MAPI によって提供される機能です。 詳細については、 [FreeProws](freeprows.md)および[FreePadrlist](freepadrlist.md)を参照してください。 **FreePadrlist** **ADRLIST**構造体のメモリと構造体のメンバーに関連付けられているすべてのメモリを解放します。**SRowSet**構造体の同じは**FreeProws**を行います。 
  
次の図は、必要な別のメモリが割り当てられたことを示す、 **ADRLIST**データ構造体のレイアウトを示しています。 灰色のボックスを表示すると、メモリを割り当てられ、1 回の呼び出しでリリースされたことができます。 
  
**ADRLIST メモリの割り当て**
  
![ADRLIST メモリの割り当て](media/amapi_52.gif "ADRLIST メモリの割り当て")
  
## <a name="see-also"></a>関連項目

- [MAPI でのメモリを管理します。](managing-memory-in-mapi.md)

