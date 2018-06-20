---
title: PidTagFlagStatus の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 38df67757082bd12e008e56632ec7e6961ba9d42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802747"
---
# <a name="pidtagflagstatus-canonical-property"></a>PidTagFlagStatus の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ オブジェクトのフラグの状態を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_FLAG_STATUS  <br/> |
|識別子:  <br/> |0x1090  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、会議に関連するオブジェクトに存在する必要があり、task オブジェクト上に存在する必要があります。 他のメッセージ オブジェクトに設定すると、このプロパティは、次の値のいずれかに設定する必要があります。
  
|**数値**|**名前**|**説明**|
|:-----|:-----|:-----|
|存在しません。  <br/> |該当なし  <br/> |フラグなし  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |完了のフラグを設定  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Flagged  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

