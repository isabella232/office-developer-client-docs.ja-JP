---
title: PidTagMiniIcon の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 04d78bddc7bae27ba23cccf676eb6e7412ffc0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803006"
---
# <a name="pidtagminiicon-canonical-property"></a>PidTagMiniIcon の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フォームの半分のサイズのアイコンのビットマップが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MINI_ICON  <br/> |
|識別子:  <br/> |0x0FFC  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

このプロパティには、内容と同じアイコンの 32 × 32 ピクセルのイメージが含まれているのです。ICO ファイルですが、左上の 16 × 16 ピクセルだけは、重要と見なされます。 このプロパティは通常からコピーします。ICO ファイルが小さい行のフォーム構成ファイルの該当する [説明] セクションで指定されています。
  
 **メモ**いくつかのプラットフォームのサポート 16 × 16 ピクセル アイコンではない操作を行います。 32 × 32 の形式このプロパティは、このようなケースでは使用できませんが、クライアント アプリケーションは表示の矛盾に注意する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagIcon の標準的なプロパティ](pidtagicon-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

