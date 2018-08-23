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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 30c8f31c104be52da2900eb81c7b7c29dfa55015
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586530"
---
# <a name="pidtagformdesignerguid-canonical-property"></a>PidTagFormDesignerGuid 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームをデザインするために使用されるオブジェクトの一意の識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FORM_DESIGNER_GUID  <br/> |
|識別子:  <br/> |0x3309  <br/> |
|データの種類 :   <br/> |PT_GUID  <br/> |
|領域:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>注釈

通常、このプロパティは、フォームの作成に使用するデザイン プログラムのグローバル一意識別子 (GUID) を含みます。 このプロパティを空にすることができます。 
  
[MAPIUID](mapiuid.md)構造体には、一意の識別子の定義が含まれています。 
  
## <a name="related-resources"></a>関連リソース

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

