---
title: PidLidSharingResponseType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a645ee26b56355c6594f5667585becbcff2e3eec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802180"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a>PidLidSharingResponseType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
共有要求の受信者が返信している応答の種類を指定します。 これは、共有メッセージのプロパティです。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidSharingResponseType  <br/> |
|プロパティを設定します。  <br/> |PSETID_Sharing  <br/> |
|長い ID (LID):  <br/> |0x00008A27  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値を次の値のいずれかに設定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |応答がありません。  <br/> |
|0x00000001  <br/> |了承済み  <br/> |
|0x00000002  <br/> |拒否  <br/> |
   
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

