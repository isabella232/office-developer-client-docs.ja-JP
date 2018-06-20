---
title: PidTagAccessLevel の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 71c0bbec13c869c1401c60834f30ca61360c8b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802411"
---
# <a name="pidtagaccesslevel-canonical-property"></a>PidTagAccessLevel の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
オブジェクトへのクライアントのアクセス レベルを示します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ACCESS_LEVEL  <br/> |
|識別子:  <br/> |0x0FF7  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |コントロール プロパティにアクセスします。  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、クライアントに対しては読み取り専用です。 次の値のいずれかを指定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |読み取り専用  <br/> |
|0x00000001  <br/> |Modify  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

