---
title: PidLidFax3EmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax3EmailAddress
api_type:
- COM
ms.assetid: 8b53c307-1a01-4c94-b6db-9fcb840ce390
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c027c165fb4ad353ceadf300ad354aef4af14d47
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577024"
---
# <a name="pidlidfax3emailaddress-canonical-property"></a>PidLidFax3EmailAddress 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
連絡先の電子メール アドレスはの他の fax アドレスを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidFax3EmailAddress  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x000080D3  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、存在する場合、含める必要があります、ユーザーが読み取り可能な表示名の後に、"@"文字、fax 番号の後に。
  
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

