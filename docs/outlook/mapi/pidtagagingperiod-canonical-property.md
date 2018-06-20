---
title: PidTagAgingPeriod の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1fd1b06bbaa10c2d7c71ee4c161fd6a980da1865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802436"
---
# <a name="pidtagagingperiod-canonical-property"></a>PidTagAgingPeriod の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
アイテムをアーカイブする前に、アイテムがフォルダーに残っている時間の長さを決定するために使用する時間単位数を表します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_AGING_PERIOD  <br/> |
|識別子:  <br/> |0x36EC  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|領域:  <br/> |その他  <br/> |
   
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

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティおよび電子メール メッセージのオブジェクトに対して許可される操作を指定します。
    
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

