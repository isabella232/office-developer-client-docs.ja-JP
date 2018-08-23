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
ms.openlocfilehash: 58037aa74cbccb67ebd480650fd0ae967a12cbf3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575694"
---
# <a name="pidlidfileunder-canonical-property"></a>PidLidFileUnder 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
連絡先の一覧を表示するときに連絡先を提出する名前を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidFileUnder  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008005  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

連絡先に表示されない場合、アプリケーションは、空の PT_UNICODE としてこのプロパティを扱う必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

