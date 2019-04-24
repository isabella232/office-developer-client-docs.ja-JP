---
title: PidLidFileUnder 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 02aa1766421f7c116eabac4c9661be1b5b1adee1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359571"
---
# <a name="pidlidfileunder-canonical-property"></a>PidLidFileUnder 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先の一覧を表示するときに、連絡先をファイリングするときの名前を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidfileunder  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x00008005  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

このプロパティが連絡先にない場合、アプリケーションはこのプロパティを空の PT_UNICODE として扱う必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

