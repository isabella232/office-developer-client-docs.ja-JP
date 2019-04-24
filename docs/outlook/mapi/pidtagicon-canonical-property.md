---
title: PidTagIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356729"
---
# <a name="pidtagicon-canonical-property"></a>PidTagIcon 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのフルサイズのアイコンのビットマップが保存されています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ICON  <br/> |
|識別子:  <br/> |0x0ffd  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI ノンノンアウトテーブル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、アイコンの32×32ピクセルのイメージが含まれています。これは、のコンテンツと同じです。.ico ファイル。 通常、このプロパティはからコピーされます。フォーム構成ファイルの該当する [Description] セクションの LargeIcon 行で指定された .ico ファイル。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagMiniIcon 標準プロパティ](pidtagminiicon-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

