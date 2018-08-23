---
title: PidLidLogFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogFlags
api_type:
- COM
ms.assetid: 3174d931-e045-44db-a203-a27c9c00f4fc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f85fdc701a29f5865700c6519d589212a06fd0af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585781"
---
# <a name="pidlidlogflags-canonical-property"></a>PidLidLogFlags 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
仕訳帳についてのメタデータが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidLogFlags  <br/> |
|プロパティを設定します。  <br/> |PSETID_Log  <br/> |
|長い ID (LID):  <br/> |0x0000870C  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |ジャーナル  <br/> |
   
## <a name="remarks"></a>注釈

仕訳帳に関するメタデータが含まれたビット フィールドは、0 または「0x40000000」のいずれかである必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> プロパティとは、仕訳帳の許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

