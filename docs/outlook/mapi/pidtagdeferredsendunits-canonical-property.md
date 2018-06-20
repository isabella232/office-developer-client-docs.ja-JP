---
title: PidTagDeferredSendUnits の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 14b1b424bc55a3a8c898eaac386a5344c2e5cf99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802659"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>PidTagDeferredSendUnits の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
**PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) のプロパティ値の乗算する時間の単位を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|識別子:  <br/> |0x3FEC  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

かどうかこのオプションを設定すると、このプロパティには次の値のいずれか。
  
|||
|:-----|:-----|
|**PidTagDeferredSendUnits** <br/> |説明  <br/> |
|0  <br/> |分、たとえば 60 秒  <br/> |
|1  <br/> |時間、たとえば 60 × 60 秒  <br/> |
|2  <br/> |日、たとえば 24 x 60 x 60 秒  <br/> |
|3  <br/> |週、たとえば 7x24x60x60 秒  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

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

