---
title: PidTagAccount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359781"
---
# <a name="pidtagaccount-canonical-property"></a>PidTagAccount 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者のアカウント名が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACCOUNT、PR_ACCOUNT_A、PR_ACCOUNT_W  <br/> |
|識別子:  <br/> |0x3A00  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、受信者の ID とアクセス情報を提供します。 受信者とその組織によって定義されます。
  
これらのプロパティには、通常、受信者の電子メール名、つまり、ローカル組織内の受信者を一意に識別する電子メール アドレスの最後のコンポーネントが含まれる。 電子メール名は X.400 識別名に対応します。これは、特定のメッセージング ドメイン内で一意である必要がある短い名前を意味します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[IMailUser : IMAPIProp](imailuserimapiprop.md)


[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

