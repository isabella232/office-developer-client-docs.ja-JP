---
title: PidTagDiscardReason の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscardReason
api_type:
- HeaderDef
ms.assetid: 5004dc1f-6bd3-4764-b83c-d04d83161dba
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4799cd14000b46053d1e571a7ab1c2c0c394a014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802685"
---
# <a name="pidtagdiscardreason-canonical-property"></a>PidTagDiscardReason の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ転送エージェント (MTA) がメッセージを破棄する理由の理由が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DISCARD_REASON  <br/> |
|識別子:  <br/> |0x0011  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

このプロパティに含まれている理由は、メッセージの配信不能レポートで使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagNonDeliveryReportReasonCode の標準的なプロパティ](pidtagnondeliveryreportreasoncode-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

