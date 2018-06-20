---
title: PidTagConversionWithLossProhibited の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: eee70d97c35c7f115e424905b9e36f3dfa392c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802654"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>PidTagConversionWithLossProhibited の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ転送エージェント (MTA) がメッセージの情報が失われるテキストの変換をすることから禁止されている場合 TRUE が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|識別子:  <br/> |0x000D  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |一般的な構成  <br/> |
   
## <a name="remarks"></a>備考

禁止されている変換の種類の例が、「損失」のマッピング Unicode (1 文字あたり 2 バイト) からシングル バイト文字セットです。 
  
## <a name="related-resources"></a>関連リソース

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

