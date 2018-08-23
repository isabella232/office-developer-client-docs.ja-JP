---
title: PidTagUserCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserCertificate
api_type:
- COM
ms.assetid: 2ac14c43-36c1-4f2f-97b0-2462f2360575
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0dd477a055562f692c8869bc436c4238c77fd02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803661"
---
# <a name="pidtagusercertificate-canonical-property"></a>PidTagUserCertificate 標準プロパティ

  
  
**適用対象**: Outlook 
  
ASN.1 にメッセージングのユーザーの認証証明書が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_USER_CERTIFICATE  <br/> |
|識別子:  <br/> |0x3A22  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI メール ユーザー  <br/> |
   
## <a name="remarks"></a>注釈

認証の証明書は、デジタル署名に似ています。 いくつかの MAPI プロパティでは、ASN.1 の証明書を提供します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

