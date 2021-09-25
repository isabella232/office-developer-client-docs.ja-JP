---
title: PidTagProviderItemId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d69ff57fd02a6f25e97c24360519f3c215b731e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574861"
---
# <a name="pidtagprovideritemid-canonical-property"></a>PidTagProviderItemId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーまたはストア内のアイテムの識別子を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_ITEMID  <br/> |
|識別子:  <br/> |0x0EA3  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MapiNonTransmittable  <br/> |
   
## <a name="remarks"></a>注釈

ストア プロバイダーは、フォルダーまたはアイテムに対してこのプロパティの値を指定できますが、セッション間で値を同じに保つ必要があります。 ストア プロバイダーは、このプロパティを使用して、検索エンジンから返される検索結果を識別します。
  
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

