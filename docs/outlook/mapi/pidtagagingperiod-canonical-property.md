---
title: PidTagAgingPeriod 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360117"
---
# <a name="pidtagagingperiod-canonical-property"></a>PidTagAgingPeriod 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムがアーカイブされる前にアイテムがフォルダー内に残っている時間の長さを判断するために使用される時間単位の数を表します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AGING_PERIOD  <br/> |
|識別子:  <br/> |0x36EC  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

アイテムがアーカイブされる前にそのアイテムがフォルダー内に残っている時間の長さは、 **PR_AGING_PERIOD**と**[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)** の2つのプロパティによって決定されます。 **PR_AGING_GRANULARITY**は、この時間の長さを決定するときに、 **PR_AGING_PERIOD**が表される時間単位を表します。 
  
**PR_AGING_GRANULARITY**に使用できる値は、次のいずれかです。 
  
****

|**[名前]**|**[説明]**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD**は、月単位で定義されます。  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD**は、週数で定義されます。  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD**は、日数で定義されています。  <br/> |
   
たとえば、アイテムがフォルダー内に2週間だけある場合に、フォルダーがアイテムをアーカイブすると、 **PR_AGING_GRANULARITY**は**AG_WEEKS**になり、 **PR_AGING_PERIOD**は2になります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本データ構造を定義します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許可されるプロパティと操作を指定します。
    
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

