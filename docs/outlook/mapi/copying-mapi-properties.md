---
title: MAPI プロパティのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2f9ee7221f523d7c92d91746f5cd719fad821a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799842"
---
# <a name="copying-mapi-properties"></a>MAPI プロパティのコピー

  
  
**適用対象**: Outlook 
  
クライアントとサービス ・ プロバイダーにコピーできます 1 つまたは複数オブジェクトのプロパティの次の**IMAPIProp**メソッドおよび API 関数をクリックすると。 
  
- [IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドは、オプションで選択したプロパティを除く、他のオブジェクトにすべてのオブジェクトのプロパティをコピーします。 **CopyTo**は、コピーまたは任意の種類のオブジェクトを移動するのに使用されます。 
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)メソッドは、オブジェクトの選択したプロパティをコピーします。 **CopyProps**は、主に使用するメッセージに使用されます。 クライアント作成する場合、メッセージの返信、転送されたコピー **CopyProps**ハンドルの元のメッセージから、適切なプロパティをコピーします。 
    
- [PropCopyMore](propcopymore.md)関数は、別に、1 つの場所から 1 つのプロパティ値をコピーします。 **PropCopyMore**を使用して、注意が必要です。 できます-一度に 1 つの値をコピーするときに-多くの小さなメモリ ブロックを割り当てるし、メモリをフラグメント化します。 
    
- [ScCopyProps](sccopyprops.md)関数では、一括でプロパティの値をコピーします。 **ScCopyProps**は、切り離されたメモリ ブロックから構築されているプロパティの値をコピーできます。 新しいプロパティの配列を返します。 
    
- **ScCopyProps**によって返されるプロパティの配列をディスクに保存する場合は、ポインターを調整する[ScRelocProps](screlocprops.md)関数を使用します。 **ScRelocProps**を 2 回呼び出す必要があります。データの操作を記述する前に、アドレスを調整するには、1 回だけ読み取り操作中にもう一度し。 **ScRelocProps**関数は、プロパティ値の配列が最初に 1 つの割り当てに割り当てられたものとします。 
    
API 関数は、上記リスト プロパティのコピーを別のオブジェクトの 1 つのオブジェクトからではなく、メモリ内で説明します。 これらの関数は現在サポートされていませんが、将来のリリースではサポートされていない可能性があります。
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

