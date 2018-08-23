---
title: PidLidDistributionListChecksum 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 44752e147569619589b23a380b2fefa511724ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571732"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a>PidLidDistributionListChecksum 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
32 ビット巡回冗長チェック (CRC 32) 多項式のチェックサムを個人用配布リストを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidDLChecksum  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x0000804C  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

既存の crc-32 を計算することによって、他の個人用配布リスト メンバーのプロパティを更新せずに、 **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) のプロパティが更新されたときを検出するためにこのプロパティの値を使用することができます。**dispidDLMembers**および**dispidDLChecksum**プロパティの値と比較することの値です。 
  
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

