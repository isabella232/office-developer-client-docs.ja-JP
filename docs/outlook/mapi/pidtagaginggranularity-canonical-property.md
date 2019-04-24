---
title: PidTagAgingGranularity 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325586"
---
# <a name="pidtagaginggranularity-canonical-property"></a>PidTagAgingGranularity 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムがアーカイブされる前に、アイテムがフォルダー内に残っている時間の長さを判断するために使用される時間の単位を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AGING_GRANULARITY  <br/> |
|識別子:  <br/> |0x36EE  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

**PR_AGING_GRANULARITY**に使用できる値は、次のいずれかです。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |.0  <br/> |**PR_AGING_PERIOD**は、月単位で定義されます。  <br/> |
|**AG_WEEKS** <br/> |1-d  <br/> |**PR_AGING_PERIOD**は、週数で定義されます。  <br/> |
|**AG_DAYS** <br/> |pbm-2  <br/> |**PR_AGING_PERIOD**は、日数で定義されています。  <br/> |
   
アイテムがアーカイブされる前にそのアイテムがフォルダー内に残っている時間の長さは、 [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)と**PR_AGING_GRANULARITY**の2つのプロパティによって決定されます。 **PR_AGING_PERIOD**は、アイテムがアーカイブされるまでフォルダー内に残っている時間単位の数を表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本データ構造を定義します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

