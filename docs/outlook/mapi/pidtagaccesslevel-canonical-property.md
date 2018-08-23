---
title: PidTagAccessLevel 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ddb667715903656291a21ebb835690768146ee9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575226"
---
# <a name="pidtagaccesslevel-canonical-property"></a>PidTagAccessLevel 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
オブジェクトへのクライアントのアクセス レベルを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACCESS_LEVEL  <br/> |
|識別子:  <br/> |0x0FF7  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |コントロール プロパティにアクセスします。  <br/> |
   
## <a name="remarks"></a>注釈

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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

