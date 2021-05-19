---
title: PidLidBusinessCardDisplayDefinition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342036"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>PidLidBusinessCardDisplayDefinition 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先を名刺として表示するためのユーザーカスタマイズの詳細が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidBCDisplayDefinition  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008040  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

名刺のレイアウトは、画像と多数のテキスト フィールドとして表されます。 画像には、連絡先写真またはカード画像を指定できます。 テキスト フィールドは、連絡先の別のプロパティ セットの値と、ユーザーが提供するオプションのカスタマイズされたラベル文字列で構成されます。 マルチバイト値は、バッファーにリトル エンド形式で格納されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

