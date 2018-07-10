---
title: PidLidSharingFlavor の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0333f0c309d89436c50a58124500f1b359584954
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802154"
---
# <a name="pidlidsharingflavor-canonical-property"></a>PidLidSharingFlavor の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
共有メッセージのプロパティとして指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidSharingFlavor  <br/> |
|プロパティを設定します。  <br/> |PSETID_Sharing  <br/> |
|長い ID (LID):  <br/> |0x00008A18  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値は、次のいずれかである必要があります。
  
|**値**|**メッセージの共有オブジェクトの種類**|
|:-----|:-----|
|0x00020310  <br/> |特殊フォルダーの共有への招待。  <br/> |
|0x00000310  <br/> |特別なフォルダーではないフォルダーの共有への招待。  <br/> |
|0x00020500  <br/> |共有の依頼です。  <br/> |
|0x00020710  <br/> |両方共有への招待の特別なフォルダーと受信者の対応する特別なフォルダーの共有の依頼です。  <br/> |
|0x00025100  <br/> |共有の応答で要求を拒否します。  <br/> |
|0x00023310  <br/> |共有の応答で (も一種の共有への招待) の要求を承諾します。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> クライアント間でのメールボックスのフォルダーを共有します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
