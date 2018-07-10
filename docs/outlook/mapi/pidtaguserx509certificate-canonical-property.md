---
title: PidTagUserX509Certificate の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d27ef47a3ba387ae2e7acbcefc75b07ddd794e80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803665"
---
# <a name="pidtaguserx509certificate-canonical-property"></a>PidTagUserX509Certificate の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージング ユーザーの X.509 version 3 のセキュリティ証明書が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_USER_X509_CERTIFICATE  <br/> |
|識別子:  <br/> |0x3A70  <br/> |
|データを入力します。  <br/> |PT_MV_BINARY  <br/> |
|領域:  <br/> |MAPI メール ユーザー  <br/> |
   
## <a name="remarks"></a>備考

公開キー セキュリティを使用するアプリケーションでこのプロパティを使用します。 1 つまたは複数の X.509 のバージョンの 3 つのセキュリティ証明書のバイナリ表現を保持します。 
  
さまざまなアプリケーションおよびクライアントは、独自のセキュリティ証明書のこのプロパティを使用できます。 X.509 データのバイナリ形式は、ベンダーの間で変更できます。 
  
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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
