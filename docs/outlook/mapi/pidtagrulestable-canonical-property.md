---
title: PidTagRulesTable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4b4b60084b8cb53a0a245b502b8fe70241fb4eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591690"
---
# <a name="pidtagrulestable-canonical-property"></a>PidTagRulesTable 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォルダーに適用されるすべてのルールを持つテーブルが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULES_TABLE  <br/> |
|識別子:  <br/> |0x3FE1  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、ルールがある、Exchange Server 上のすべてのフォルダー オブジェクト上に存在します。 このプロパティに含まれる値は、読み取りとルールを変更するのに使用されます。 **IID_IExchangeModifyTable**インターフェイス識別子を使用して[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを使用するにを取得するのには、 [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)フォルダーのルール テーブルへのインターフェイスです。 読み取りおよびそれらの規則を変更するには、このインターフェイスを使用します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。 
    
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

