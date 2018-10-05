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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401105"
---
# <a name="pidtagaccount-canonical-property"></a>PidTagAccount 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者のアカウント名が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACCOUNT、PR_ACCOUNT_A、PR_ACCOUNT_W  <br/> |
|識別子:  <br/> |0x3A00  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。 受信者とその構造によって定義されます。
  
通常、これらのプロパティには、受信者の電子メール名、電子メール アドレスは、ローカル組織内の受信者を一意に識別するは、最終的なコンポーネントが含まれています。 電子メール名は、短い形式の名前が特定のメッセージング ドメイン内で一意であることを保証するものでは X.400 の識別名に対応します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[IMailUser : IMAPIProp](imailuserimapiprop.md)


[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

