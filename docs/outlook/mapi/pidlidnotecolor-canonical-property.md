---
title: PidLidNoteColor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidNoteColor
api_type:
- COM
ms.assetid: 9d4b8f5f-1789-497c-8010-f83da9ba5966
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c07460767ab1684fd67dd6e4db8a29912ca6b45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604580"
---
# <a name="pidlidnotecolor-canonical-property"></a>PidLidNoteColor 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メモの背景色を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidNoteColor  <br/> |
|プロパティ セット:  <br/> |PSETID_Note  <br/> |
|長い ID (LID):  <br/> |0x00008B00  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |付箋  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、次の表のエントリの 1 つである必要があります。
  
|**値**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |青  <br/> |
|0x00000001  <br/> |緑  <br/> |
|0x00000002  <br/> |Pink  <br/> |
|0x00000003  <br/> |黄  <br/> |
|0x00000004  <br/> |ホワイト  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXONOTE]](https://msdn.microsoft.com/library/6bf4ed7e-316c-4a3c-be27-5ec93e7ab39f%28Office.15%29.aspx)
  
> メモで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

