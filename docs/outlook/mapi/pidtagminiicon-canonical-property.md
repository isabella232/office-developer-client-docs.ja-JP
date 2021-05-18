---
title: PidTagMiniIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405416"
---
# <a name="pidtagminiicon-canonical-property"></a>PidTagMiniIcon 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのハーフサイズ アイコンのビットマップを含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MINI_ICON  <br/> |
|識別子:  <br/> |0x0FFC  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、アイコンの 32 × 32 ピクセルの画像が含まれる。これは、 の内容と同じです。ICO ファイルですが、左上 16 ピクセル× 16 ピクセルだけが重要と見なされます。 このプロパティは、通常は . からコピーされます。フォーム構成ファイルの適切な [Description] セクションの SmallIcon 行で指定された ICO ファイル。
  
 **メモ** 一部のプラットフォームでは、16 ピクセル×アイコンがサポートされていません。 このプロパティの 32 × 32 形式は、このような場合に使用できますが、クライアント アプリケーションは、表示の不整合に注意する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagIcon 標準プロパティ](pidtagicon-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

