---
title: PidNameXSharingFlavor の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1f07a11c47c6785bc9a166f11bde8f2e5ef464a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802386"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>PidNameXSharingFlavor の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
**DispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) プロパティの値を表します。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |なし  <br/> |
|プロパティを設定します。  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |X 共有フレーバー  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>備考

**DispidSharingFlavor**プロパティは、次の値のいずれかである必要があります。 
  
|**値**|**共有メッセージの種類**|
|:-----|:-----|
|0x00020310  <br/> |特殊フォルダーの共有への招待。  <br/> |
|0x00000310  <br/> |特別なフォルダーではないフォルダーの共有への招待。  <br/> |
|0x00020500  <br/> |共有の依頼です。  <br/> |
|0x00020710  <br/> |両方共有への招待の特別なフォルダーと受信者の対応する特別なフォルダーの共有の依頼です。  <br/> |
|0x00025100  <br/> |共有の応答、要求を拒否します。  <br/> |
|0x00023310  <br/> |共有の応答 (も一種の共有への招待) の要求を受け入れる。  <br/> |
   
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

