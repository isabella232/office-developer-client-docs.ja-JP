---
title: PidTagExpiryUnits 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c753bb84ccbfe2fa6869d56806fd042a6d60e9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802725"
---
# <a name="pidtagexpiryunits-canonical-property"></a>PidTagExpiryUnits 標準プロパティ

  
  
**適用対象**: Outlook 
  
**PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) のプロパティを乗算すると時間の単位について説明します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXPIRY_UNITS  <br/> |
|識別子:  <br/> |0x3FEE  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティでは場合は、次の値のいずれかである必要があります。
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |説明 (水曜)  <br/> |
|0x00000000  <br/> |分、たとえば 60 秒  <br/> |
|0x00000001  <br/> |時間、たとえば 60 × 60 秒  <br/> |
|0x00000002  <br/> |日、たとえば 24 x 60 x 60 秒  <br/> |
|0x00000003  <br/> |週、たとえば 7x24x60x60 秒  <br/> |
   
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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

