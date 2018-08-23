---
title: MAPI プロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803795"
---
# <a name="saving-mapi-properties"></a>MAPI プロパティの保存

  
  
**適用対象**: Outlook 
  
多くのオブジェクトは、トランザクション モデルのため、プロパティを変更できない永続的なものは後でコミットされるまでの処理をサポートします。 プロパティへの変更は、 [IMAPIProp::SetProps](imapiprop-setprops.md)および[IMAPIProp::DeleteProps](imapiprop-deleteprops.md)メソッドは、一方、commit の手順は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)によって処理されます。 **失敗 savechanges メソッド**の呼び出し、最新のオブジェクトのプロパティにアクセスできることが終了するまでではありません。 
  
**SaveChanges**には、エラー値 MAPI_E_OBJECT_CHANGED が返された、これは、する別のクライアントが同時に変更をコミットするオブジェクトに警告します。 可能性が、複数のクライアントに対して、オブジェクトを実装すると、正常にプロバイダーによってオブジェクトを開くメソッドを呼び出して、 **OpenEntry** 、MAPI_MODIFY フラグを設定して読み取り/書き込みアクセス許可を付与します。 **OpenEntry**呼び出しは、ストレージ ・ データのスナップショットではこのような返されるオブジェクト。 各とするとこのデータを変更するには、以前の試みを上書きできます。 
  
クライアントでは、 **SaveChanges**から MAPI_E_OBJECT_CHANGED を受信時にするオプションがあります。 
  
- 変更を保持するオブジェクトのコピーを作成します。
    
- **SaveChanges**FORCE_SAVE を指定する別の呼び出しを確認します。 
    
FORCE_SAVE フラグを使用して**SaveChanges**を呼び出すことでは、前回の保存が上書きされ、クライアントの変更を永続的になります。 
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

