---
title: PidTagSurname 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSurname
api_type:
- COM
ms.assetid: 1663f032-4cdc-43ed-8fdc-a91a3a6a84ff
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 82f4e7f1d275ad47679aaaa9ad6e4d0f69d54bc1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391186"
---
# <a name="pidtagsurname-canonical-property"></a>PidTagSurname 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最後または受信者の姓が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SURNAME、PR_SURNAME_A、PR_SURNAME_W  <br/> |
|識別子:  <br/> |0x3A11  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI メール ユーザー  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。 受信者と受信者の組織によって定義されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

