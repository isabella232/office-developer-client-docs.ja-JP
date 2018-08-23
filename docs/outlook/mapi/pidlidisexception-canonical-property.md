---
title: PidLidIsException 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b1d4600810d4f773896f1880b7309c1f818c7dc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575778"
---
# <a name="pidlidisexception-canonical-property"></a>PidLidIsException 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
示します (孤立したインスタンスを含む)、例外を表すオブジェクト。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |LID_IS_EXCEPTION  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x0000000A  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

FALSE の値を示します定期的または 1 つのインスタンスを表すオブジェクト。 任意のオブジェクトに対してこのプロパティがない場合は、TRUE の値では例外の埋め込みメッセージを除いて FALSE の値を示します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

