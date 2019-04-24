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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333076"
---
# <a name="copying-mapi-properties"></a>MAPI プロパティのコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントおよびサービスプロバイダーは、次の**imapiprop**メソッドと API 関数を使用して、1つ以上のオブジェクトのプロパティをコピーできます。 
  
- [imapiprop:: CopyTo](imapiprop-copyto.md)メソッドは、必要に応じて、選択したプロパティを除外して、オブジェクトのすべてのプロパティを別のオブジェクトにコピーします。 **CopyTo**は、任意の種類のオブジェクトをコピーまたは移動するために使用されます。 
    
- [imapiprop:: copyprops](imapiprop-copyprops.md)メソッドは、オブジェクトの選択されたプロパティをコピーします。 **copyprops**は、主にメッセージで使用されます。 クライアントがメッセージの転送コピーまたは応答を作成すると、 **copyprops**は、元のメッセージから適切なプロパティをコピーする処理を行います。 
    
- [propcopymore](propcopymore.md)関数は、1つのプロパティ値をある場所から別の場所にコピーします。 **propcopymore**は慎重に使用してください。 これは、一度に1つの値をコピーするときに、少数のメモリブロックを割り当て、メモリをフラグメント化することができます。 
    
- [sccopyprops](sccopyprops.md)関数は、プロパティの値を一括でコピーします。 **sccopyprops**では、メモリブロックのないメモリブロックから構築されたプロパティ値をコピーできます。 このメソッドは、新しいプロパティ配列を返します。 
    
- **sccopyprops**によって返されるプロパティの配列をディスクに格納する場合は、 [ScRelocProps](screlocprops.md)関数を使用してポインターを調整します。 **ScRelocProps**は2回呼び出す必要があります。データ操作を書き込む前にアドレスを調整した後、読み取り操作中に再びアドレスを調整します。 **ScRelocProps**関数は、プロパティ値の配列が最初は単一の割り当てで割り当てられていることを前提としています。 
    
前のリストで説明した API 関数は、オブジェクトから別のオブジェクトへのプロパティではなく、メモリ内のプロパティをコピーします。 これらの関数は現在サポートされていますが、今後のリリースではサポートされない可能性があります。
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

