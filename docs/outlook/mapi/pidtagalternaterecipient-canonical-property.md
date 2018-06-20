---
title: PidTagAlternateRecipient の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ea78d9487e4929c2df3d49a9b85ba4aefac90a59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802438"
---
# <a name="pidtagalternaterecipient-canonical-property"></a>PidTagAlternateRecipient の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
元の受信者が指定されている代替の受信者のエントリの識別子の一覧が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ALTERNATE_RECIPIENT  <br/> |
|識別子:  <br/> |0x3A01  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>備考

自動転送済みのメッセージにこのプロパティが使用されます。 代理受信者の[FLATENTRYLIST](flatentrylist.md)構造体が含まれています。 自動転送が許可されていない場合、または別の受信者が指定されていない場合は、配信不能レポートが生成されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[FLATENTRYLIST](flatentrylist.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

