---
title: PidTagAgingGranularity の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 09a79a68d7619ded9edf3ec4ac67733bdec1e32c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802448"
---
# <a name="pidtagaginggranularity-canonical-property"></a>PidTagAgingGranularity の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
アイテムをアーカイブする前に、アイテムがフォルダーに残って時間の長さを決定するために使用される時間の単位を表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_AGING_GRANULARITY  <br/> |
|識別子:  <br/> |0x36EE  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>備考

**PR_AGING_GRANULARITY**の有効な値には、次のいずれかを指定できます。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |0  <br/> |**PR_AGING_PERIOD**は、月の数で定義されます。  <br/> |
|**AG_WEEKS** <br/> |1  <br/> |**PR_AGING_PERIOD**は、週数で定義されます。  <br/> |
|**AG_DAYS** <br/> |2  <br/> |**PR_AGING_PERIOD**は、日数で定義されます。  <br/> |
   
アイテムをアーカイブする前に、アイテムがフォルダーに残っている時間の長さは、 [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)と**PR_AGING_GRANULARITY**の 2 つのプロパティによって決定されます。 **PR_AGING_PERIOD**では、アーカイブする前に、アイテムがフォルダーに残っている時間の単位の数を表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

