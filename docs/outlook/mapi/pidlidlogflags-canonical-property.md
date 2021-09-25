---
title: PidLidLogFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidLogFlags
api_type:
- COM
ms.assetid: 3174d931-e045-44db-a203-a27c9c00f4fc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c46478ba531742d0df96878993df77e2bb033f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624896"
---
# <a name="pidlidlogflags-canonical-property"></a>PidLidLogFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ジャーナルに関するメタデータが含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidLogFlags  <br/> |
|プロパティ セット:  <br/> |PSETID_Log  <br/> |
|長い ID (LID):  <br/> |0x0000870C  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |ジャーナル  <br/> |
   
## <a name="remarks"></a>注釈

ジャーナルに関するメタデータを含むビット フィールドは、ゼロまたは "0x40000000" である必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> ジャーナルに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

