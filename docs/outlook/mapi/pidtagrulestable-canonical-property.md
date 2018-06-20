---
title: PidTagRulesTable の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 945dabec4ee34d38d2474c918e779d894f4a917c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803427"
---
# <a name="pidtagrulestable-canonical-property"></a>PidTagRulesTable の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フォルダーに適用されるすべてのルールを持つテーブルが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RULES_TABLE  <br/> |
|識別子:  <br/> |0x3FE1  <br/> |
|データを入力します。  <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、ルールがある、Exchange Server 上のすべてのフォルダー オブジェクト上に存在します。 このプロパティに含まれる値は、読み取りとルールを変更するのに使用されます。 **IID_IExchangeModifyTable**インターフェイス識別子を使用して[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを使用するにを取得するのには、 [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)フォルダーのルール テーブルへのインターフェイスです。 読み取りおよびそれらの規則を変更するには、このインターフェイスを使用します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。 
    
## <a name="see-also"></a>関連項目



[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

