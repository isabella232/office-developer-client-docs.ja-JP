---
title: PidTagIpmSubtreeEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a68227c61abe65f785739e42a2d09a01ba6ef3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583402"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a>PidTagIpmSubtreeEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアのフォルダー ツリー内の対人間メッセージ (IPM) フォルダー サブツリーのルートのエントリ識別子を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IPM_SUBTREE_ENTRYID  <br/> |
|識別子:  <br/> |0x35E0  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |フォルダー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、IPM 階層のルートを表します。 IPM クライアントには、このプロパティで表されるフォルダーのサブフォルダーではないフォルダーは表示されません。
  
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

