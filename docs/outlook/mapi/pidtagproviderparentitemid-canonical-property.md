---
title: PidTagProviderParentItemId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a0c8af1cc36fe7f3e4c97023381e0036fed18ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574819"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>PidTagProviderParentItemId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの親またはストア内のアイテムの識別子を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|識別子:  <br/> |0x0EA4  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

ストア プロバイダーは、フォルダーまたはアイテムの親に対してこのプロパティの値を指定できますが、セッション間で値を同じに保つ必要があります。 ストア プロバイダーは、このプロパティを使用して、検索エンジンから返される検索結果を識別します。
  
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

