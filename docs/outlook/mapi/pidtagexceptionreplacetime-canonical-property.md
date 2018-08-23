---
title: PidTagExceptionReplaceTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExceptionReplaceTime
api_type:
- HeaderDef
ms.assetid: bd4d1311-15e4-4275-a967-c6d11d2e48d2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 20893f7c3d64698f70ae26c09c2d7ddc64ce3f9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569933"
---
# <a name="pidtagexceptionreplacetime-canonical-property"></a>PidTagExceptionReplaceTime 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
元の日付と時間のパターン内のインスタンスがあるが発生した場合例外でされていない場合を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXCEPTION_REPLACETIME  <br/> |
|識別子:  <br/> |0x7FF9  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |クラスによって定義されたメッセージの転送を可能な  <br/> |
   
## <a name="remarks"></a>注釈

この値は、世界協定時刻 (UTC) で指定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

