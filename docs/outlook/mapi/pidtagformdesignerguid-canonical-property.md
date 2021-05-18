---
title: PidTagFormDesignerGuid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b0e0847a3a9e21f080a852738ec8afbc98a2263f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412241"
---
# <a name="pidtagformdesignerguid-canonical-property"></a>PidTagFormDesignerGuid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの設計に使用されるオブジェクトの一意の識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FORM_DESIGNER_GUID  <br/> |
|識別子:  <br/> |0x3309  <br/> |
|データの種類 :   <br/> |PT_GUID  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

通常、このプロパティには、フォームの作成に使用されるデザイン プログラムのグローバル一意識別子 (GUID) が含まれる。 このプロパティは空の場合があります。 
  
[MAPIUID 構造体には](mapiuid.md)、一意の識別子の定義が含まれる。 
  
## <a name="related-resources"></a>関連リソース

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

