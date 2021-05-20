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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428502"
---
# <a name="pidtagrulestable-canonical-property"></a>PidTagRulesTable 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーに適用されるすべてのルールを含むテーブルが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULES_TABLE  <br/> |
|識別子:  <br/> |0x3FE1  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、ルールを持つオブジェクト上Exchange Serverに存在します。 このプロパティに含まれる値は、ルールの読み取りおよび変更に使用されます。 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを **IID_IExchangeModifyTable** インターフェイス識別子と一緒に使用して [、IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)インターフェイスをフォルダーのルール テーブルに取得できます。 このインターフェイスを使用して、これらのルールを読み取り、変更できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。 
    
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

