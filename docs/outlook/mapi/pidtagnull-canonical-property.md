---
title: PidTagNull の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 55db507055692c9e929b0125abf719d8c03ac967
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803039"
---
# <a name="pidtagnull-canonical-property"></a>PidTagNull の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
配列の領域を予約または、null 値またはプロパティの設定を表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_NULL  <br/> |
|識別子:  <br/> |0x0000  <br/> |
|データを入力します。  <br/> |PT_NULL  <br/> |
|領域:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>備考

[SPropValue](spropvalue.md)構造体の配列の領域を予約するのにはこのプロパティを使用します。 **SPropValue**構造体の返される配列内の領域を予約する方法を指示する[SPropTagArray](sproptagarray.md)構造体の配列で使用されます。 安価な方法で設定されるプロパティを計算できます。 
  
詳細については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許可されている操作のプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

