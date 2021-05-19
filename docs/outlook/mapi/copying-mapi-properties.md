---
title: MAPI プロパティのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415048"
---
# <a name="copying-mapi-properties"></a>MAPI プロパティのコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントとサービス プロバイダーは、次の **IMAPIProp** メソッドと API 関数を使用して、1 つ以上のオブジェクトのプロパティをコピーできます。 
  
- [IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドは、オブジェクトのすべてのプロパティを別のオブジェクトにコピーします。必要に応じて、選択したプロパティを除外します。 **CopyTo** は、任意の種類のオブジェクトをコピーまたは移動するために使用されます。 
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)メソッドは、オブジェクトの選択したプロパティをコピーします。 **CopyProps は** 主にメッセージと一緒に使用されます。 クライアントがメッセージまたは返信の転送されたコピーを作成すると **、CopyProps は** 元のメッセージから適切なプロパティのコピーを処理します。 
    
- [PropCopyMore](propcopymore.md)関数は、1 つのプロパティ値を 1 つの場所から別の場所にコピーします。 **PropCopyMore を使用する場合は** 注意が必要です。 一度に 1 つの値をコピーするときに、メモリの小さいブロックを多数割り当て、メモリをフラグメント化することができます。 
    
- [ScCopyProps 関数は](sccopyprops.md)、プロパティ値を一括でコピーします。 **ScCopyProps は** 、不一部のメモリ ブロックから構築されたプロパティ値をコピーできます。 新しいプロパティ配列を返します。 
    
- **ScCopyProps** によって返されるプロパティ配列をディスクに格納する場合は [、ScRelocProps](screlocprops.md)関数を使用してポインターを調整します。 **ScRelocProps は** 2 回呼び出す必要があります。データ操作を書き込む前にアドレスを調整してから、読み取り操作中にもう一度アドレスを調整します。 **ScRelocProps 関数** は、プロパティ値配列が最初に 1 つの割り当てで割り当てられたと仮定します。 
    
前述のリスト で説明した API 関数は、オブジェクト間ではなくメモリ内のプロパティをコピーします。 これらの関数は現在サポートされますが、今後のリリースではサポートされない可能性があります。
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

