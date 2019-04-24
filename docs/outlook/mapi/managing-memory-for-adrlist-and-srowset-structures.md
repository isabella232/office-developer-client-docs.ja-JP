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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298130"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>adrlist および srowset 構造体のメモリの管理 "

**適用対象**: Outlook 2013 | Outlook 2016 
  
単一の**MAPIAllocateBuffer**呼び出しで、可能な場合には、アドレス一覧、 **adrlist**、行セット、または**srowset**、構造体を使用している場合には、バッファーのすべてのメモリを割り当てる必要があります。 
  
これらの2つの構造体は、メモリを割り当てて解放するための標準的な規則の例外です。 複数のレベルの構造が含まれており、個々のメンバーを追加または削除できるように設計されています。 そのため、各プロパティは個別に割り当てる必要があります。 

ほとんどの構造体は**MAPIFreeBuffer**への呼び出しによって解放されます。 **adrlist**構造体または**srowset**構造体内の個々のエントリは、 **MAPIFreeBuffer**への独自の呼び出し、または**freeprows**への1回の呼び出しで解放する必要があります。または **、freepadrlist**。 詳細については、「 [MAPIFreeBuffer](mapifreebuffer.md)」、「 [adrlist](adrlist.md)」、および「 [srowset](srowset.md)」を参照してください。 

**freeprows**および**freepadrlist**は、これらのデータ構造の解放を簡略化するために MAPI によって提供される機能です。 詳細については、「 [freeprows](freeprows.md) 」および「 [freepadrlist](freepadrlist.md)」を参照してください。 **freepadrlist**は、 **adrlist**構造体のメモリと、構造体メンバーに関連付けられているすべてのメモリを解放します。**freeprows**は、 **srowset**構造に対して同じことを行います。 
  
次の図は、 **adrlist**データ構造のレイアウトを示しています。これは、別のメモリ割り当てが必要であることを示します。 灰色のボックスには、1回の呼び出しで割り当てたり解放したりできるメモリが表示されます。 
  
**ADRLIST メモリの割り当て**
  
![adrlist のメモリ割り当て](media/amapi_52.gif "adrlist のメモリ割り当て")
  
## <a name="see-also"></a>関連項目

- [MAPI でのメモリの管理](managing-memory-in-mapi.md)

