---
title: PidNameRightsManagementLicense の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c75cb480b9a1a7ffdcff9c0f9b49aabba746fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802372"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>PidNameRightsManagementLicense の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
権限が管理された電子メール メッセージの使用ライセンスをキャッシュします。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |なし  <br/> |
|プロパティを設定します。  <br/> |PS_PUBLIC_STRINGS  <br/> |
|プロパティ名:  <br/> |DRMLicense  <br/> |
|データを入力します。  <br/> |PT_MV_BINARY  <br/> |
|領域:  <br/> |メッセージのセキュリティ保護します。  <br/> |
   
## <a name="remarks"></a>備考

権限が管理された電子メール メッセージのプロパティがある場合、この複数のバイナリ プロパティの最初の値は、([RFC1950] で指定) と同じ ZLIB 圧縮使用ライセンスを権限管理された電子メール メッセージを含める必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限管理でエンコードされたメッセージのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

