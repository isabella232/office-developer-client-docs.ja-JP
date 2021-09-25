---
title: PidLidSmartNoAttach 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f73e45038aac9da37519440efce38a4085f83cf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630189"
---
# <a name="pidlidsmartnoattach-canonical-property"></a>PidLidSmartNoAttach 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの添付ファイルが非表示と見なされるかどうかを表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidSmartNoAttach  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008514  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>注釈

メッセージの添付ファイルが非表示と見なされる場合、このプロパティは TRUE です。
  
メッセージ オブジェクトにエンド ユーザーに表示される添付ファイルがないかどうかを示します。 このプロパティは設定されていない可能性があります。この場合、既定値は FALSE と見なされます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様Exchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

