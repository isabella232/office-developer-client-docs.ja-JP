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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391179"
---
# <a name="pidtagagingperiod-canonical-property"></a>PidTagAgingPeriod 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムをアーカイブする前に、アイテムがフォルダーに残っている時間の長さを決定するために使用する時間単位数を表します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AGING_PERIOD  <br/> |
|識別子:  <br/> |0x36EC  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>備考

アイテムをアーカイブする前に、アイテムがフォルダーに残っている時間の長さは、 **PR_AGING_PERIOD**と**[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)** の 2 つのプロパティによって決定されます。 **PR_AGING_GRANULARITY**は、 **PR_AGING_PERIOD**が表現する、この期間を決定する際に時間の単位を表します。 
  
**PR_AGING_GRANULARITY**の有効な値には、次のいずれかを指定できます。 
  
****

|**名前**|**説明**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD**は、月の数で定義されます。  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD**は、週数で定義されます。  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD**は、日数で定義されます。  <br/> |
   
たとえば、アイテムのフォルダーに、2 週間後で**PR_AGING_GRANULARITY**された後にのみアイテムがフォルダーのアーカイブの場合**AG_WEEKS**と**PR_AGING_PERIOD**は 2 です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティおよび電子メール メッセージのオブジェクトに対して許可される操作を指定します。
    
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

