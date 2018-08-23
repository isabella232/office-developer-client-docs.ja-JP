---
title: PidTagConversionWithLossProhibited 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e5d9261a9f33d77d52cfd6e448e69a2c1e8df415
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585235"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>PidTagConversionWithLossProhibited 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ転送エージェント (MTA) がメッセージの情報が失われるテキストの変換をすることから禁止されている場合 TRUE が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|識別子:  <br/> |0x000D  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |一般的な構成  <br/> |
   
## <a name="remarks"></a>注釈

禁止されている変換の種類の例が、「損失」のマッピング Unicode (1 文字あたり 2 バイト) からシングル バイト文字セットです。 
  
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

