---
title: PidTagProviderItemId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e0f13b0b8d2f7eb6fd7ba60e9e351b62251aa13d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572838"
---
# <a name="pidtagprovideritemid-canonical-property"></a>PidTagProviderItemId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストア内のフォルダーまたはアイテムの識別子を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_ITEMID  <br/> |
|識別子:  <br/> |0x0EA3  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MapiNonTransmittable  <br/> |
   
## <a name="remarks"></a>注釈

ストア プロバイダーは、フォルダーまたはアイテムのこのプロパティの値を指定できますが、セッション間で同じように値が保持する必要があります。 ストア プロバイダーは、検索エンジンから返される検索結果を識別するのには、このプロパティを使用します。
  
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

