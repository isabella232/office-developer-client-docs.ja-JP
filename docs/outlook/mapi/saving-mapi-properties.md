---
title: MAPI プロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425891"
---
# <a name="saving-mapi-properties"></a>MAPI プロパティの保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くのオブジェクトは処理のトランザクションモデルをサポートしているため、プロパティへの変更は後でコミットされるまで永続的に行われません。 プロパティへの変更は[imapiprop:: setprops](imapiprop-setprops.md)メソッドと[imapiprop::D eleteprops](imapiprop-deleteprops.md)メソッドによって処理されますが、コミット手順は[imapiprop:: SaveChanges](imapiprop-savechanges.md)によって処理されます。 これは、オブジェクトのプロパティの最新バージョンにアクセスできるように**SaveChanges**を正常に呼び出した後には行われません。 
  
**SaveChanges**がエラー値 MAPI_E_OBJECT_CHANGED を返す場合、これは、別のクライアントがオブジェクトへの変更を同時にコミットしていることを示す警告です。 オブジェクトを実装するプロバイダーによっては、MAPI_MODIFY フラグが設定された**openentry**メソッドを呼び出して読み取り/書き込みアクセス権を付与することによって、複数のクライアントがオブジェクトを正常に開くことができます。 このような**openentry**呼び出しから返されるオブジェクトは、ストレージデータのスナップショットです。 このデータを以降に変更しようとするたびに、以前の試行を上書きできます。 
  
MAPI_E_OBJECT_CHANGED を**SaveChanges**から受け取る際に、クライアントには次のオプションがあります。 
  
- 変更を保持するオブジェクトのコピーを作成します。
    
- FORCE_SAVE を指定して、再度、 **SaveChanges**を呼び出してください。 
    
FORCE_SAVE フラグを使用して**SaveChanges**を呼び出すと、以前の保存が上書きされ、クライアントの変更が永続的に行われます。 
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

