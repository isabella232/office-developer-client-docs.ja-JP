---
title: PidTagagingPeriod 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360117"
---
# <a name="pidtagagingperiod-canonical-property"></a>PidTagagingPeriod 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムがアーカイブされる前にアイテムがフォルダーに残る時間の長さを決定するために使用される時間単位の数を表します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AGING_PERIOD  <br/> |
|識別子:  <br/> |0x36EC  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

アイテムがアーカイブされる前にアイテムがフォルダー内に残る時間の長さは、2 つのプロパティ **、PR_AGING_PERIODと** PR_AGING_GRANULARITY。 **[](pidtagaginggranularity-canonical-property.md)** **PR_AGING_GRANULARITY** は、この時間の長さを決定するときにPR_AGING_PERIODを表す時間単位を表します。 
  
指定できる値は **PR_AGING_GRANULARITY** のいずれかを指定できます。 
  
****

|**名前**|**説明**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** は月数で定義されます。  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** 週数で定義されます。  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** は日数で定義されます。  <br/> |
   
たとえば、アイテムが 2 週間フォルダーに保存された後にのみフォルダーがアイテムをアーカイブする場合 **、PR_AGING_GRANULARITY** は AG_WEEKS、PR_AGING_PERIOD は2 です。  
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許可されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

