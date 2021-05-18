---
title: PidTagUserX509Certificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e6446283116c39080271e5c2fb3ec128b25d32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360719"
---
# <a name="pidtaguserx509certificate-canonical-property"></a>PidTagUserX509Certificate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング ユーザーの X.509 バージョン 3 セキュリティ証明書が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_USER_X509_CERTIFICATE  <br/> |
|識別子:  <br/> |0x3A70  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |MAPI メール ユーザー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、公開キーのセキュリティを利用するアプリケーションで使用されます。 1 つ以上の X.509 バージョン 3 セキュリティ証明書のバイナリ表現を保持します。 
  
さまざまなアプリケーションとクライアントは、独自のセキュリティ証明書にこのプロパティを使用できます。 X.509 データのバイナリ形式はベンダーによって異なります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

