---
title: MAPI プロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2db022929516caa6b0aaad96d8e1997b70249546
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599082"
---
# <a name="saving-mapi-properties"></a>MAPI プロパティの保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くのオブジェクトは処理のトランザクション モデルをサポートしています。その結果、プロパティに対する変更は、後でコミットされるまで永続化されません。 プロパティへの変更は [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドと [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) メソッドによって処理されるのに対し、コミット ステップは [IMAPIProp::SaveChanges](imapiprop-savechanges.md)によって処理されます。 **SaveChanges** の呼び出しが成功するまで、オブジェクトのプロパティの最新バージョンにアクセスできます。 
  
**SaveChanges が** エラー値を返MAPI_E_OBJECT_CHANGED、これは、別のクライアントがオブジェクトに対する変更を同時にコミットしているという警告です。 オブジェクトを実装するプロバイダーによっては、複数のクライアントが MAPI_MODIFY フラグ セットを使用して **OpenEntry** メソッドを呼び出してオブジェクトを正常に開き、読み取り/書き込みアクセス権を与えることも可能です。 このような **OpenEntry** 呼び出しから返されるオブジェクトは、ストレージ データのスナップショットです。 以降、このデータを変更しようとすると、以前の試行が上書きされる可能性があります。 
  
**SaveChanges** MAPI_E_OBJECT_CHANGED受信すると、クライアントは次のオプションを使用できます。 
  
- 変更を保持するオブジェクトのコピーを作成します。
    
- SaveChanges に別の **呼び出しを行** い、名前をFORCE_SAVE。 
    
**SaveChanges を呼** び出して FORCE_SAVEフラグを指定すると、以前の保存が上書きされ、クライアントの変更が永続的になります。 
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

