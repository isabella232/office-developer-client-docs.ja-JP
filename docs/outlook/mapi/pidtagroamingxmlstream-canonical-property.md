---
title: PidTagRoamingXmlStream 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingXmlStream
api_type:
- COM
ms.assetid: ce55b50e-3dbf-4690-9102-c08f35ada82e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3e7ce1f810a1dd37cd4370ceb423b664d75878a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359543"
---
# <a name="pidtagroamingxmlstream-canonical-property"></a>PidTagRoamingXmlStream 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
任意の XML ストリームを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROAMING_XMLSTREAM  <br/> |
|識別子:  <br/> |0x7C08  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |構成  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、XML データの任意のストリームが含まれます。 メッセージ内の他のプロパティは、このプロパティで使用する特定のスキーマを示している可能性があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

