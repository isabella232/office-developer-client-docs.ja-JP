---
title: PidTagCountry の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCountry
api_type:
- HeaderDef
ms.assetid: c9470496-fb37-4019-ae1b-b4f93ac55048
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f9c09e963ecbb5ddeecff1ad43e021d8718e0729
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802658"
---
# <a name="pidtagcountry-canonical-property"></a>PidTagCountry の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
受信者の国または地域の名前が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_COUNTRY、PR_COUNTRY_A、PR_COUNTRY_W、PR_BUSINESS_ADDRESS_COUNTRY、PR_BUSINESS_ADDRESS_COUNTRY_A、PR_BUSINESS_ADDRESS_COUNTRY_W  <br/> |
|識別子:  <br/> |0x3A26  <br/> |
|データを入力します。  <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティでは、id、および受信者に関する情報にアクセスを提供するプロパティの例を示します。 これらのプロパティは、受信者と受信者の組織によって定義されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
