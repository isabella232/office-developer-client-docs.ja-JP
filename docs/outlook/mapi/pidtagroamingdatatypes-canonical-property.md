---
title: PidTagRoamingDatatypes 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384263"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>PidTagRoamingDatatypes 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティがメッセージに存在するストリームを示すビットマスクを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|識別子:  <br/> |0x7C06  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Configuration  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、次の値の 1 つ以上に設定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000002  <br/> |フォルダー関連情報 (FAI) メッセージに固定の XML スキーマとしてシリアル化され、 **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) のプロパティに格納されている辞書のストリームが含まれている必要があることを示します。 FAI メッセージに辞書のストリームが含まれていない場合、アプリケーションは、エントリがないものとして、辞書を扱う必要があります。  <br/> |
|0x00000004  <br/> |FAI メッセージに任意の XML スキーマを使用する**PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) のプロパティに格納されている XML ストリームが含まれている必要があることを示します。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。
    
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

