---
title: PidTagIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 90ca5cef741f69d68f1db06098ca8133720a8130
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555350"
---
# <a name="pidtagicon-canonical-property"></a>PidTagIcon 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのフル サイズ アイコンのビットマップを含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ICON  <br/> |
|識別子:  <br/> |0x0FFD  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、アイコンの 32 × 32 ピクセルの画像が含まれる。これは、 の内容と同じです。ICO ファイル。 このプロパティは、通常は . からコピーされます。フォーム構成ファイルの適切な [Description] セクションの LargeIcon 行で指定された ICO ファイル。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagMiniIcon 標準プロパティ](pidtagminiicon-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

