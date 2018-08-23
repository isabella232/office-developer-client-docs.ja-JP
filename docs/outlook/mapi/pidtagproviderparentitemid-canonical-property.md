---
title: PidTagProviderParentItemId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d0ec4e793a5b7940802ee159c2e869695166ce93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563283"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>PidTagProviderParentItemId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォルダーまたはストア内のアイテムの親の識別子を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|識別子:  <br/> |0x0EA4  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>注釈

ストア プロバイダーは、フォルダーまたはアイテムの親に対してこのプロパティの値を指定できますが、セッション間で同じように値が保持する必要があります。 ストア プロバイダーは、検索エンジンから返される検索結果を識別するのには、このプロパティを使用します。
  
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

