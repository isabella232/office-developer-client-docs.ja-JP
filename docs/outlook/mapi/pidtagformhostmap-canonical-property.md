---
title: PidTagFormHostMap 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a8c7869e6bcfc926e071b386cc70f446b537ac28
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587679"
---
# <a name="pidtagformhostmap-canonical-property"></a>PidTagFormHostMap 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
使用可能なフォームのホスト マップが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FORM_HOST_MAP  <br/> |
|識別子:  <br/> |0x3306  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

**IMAPIFormProp** インターフェイスで基になる構造を変更 **する場合、クライアント** アプリケーションは PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと共にこのプロパティを更新する必要があります。 
  
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

