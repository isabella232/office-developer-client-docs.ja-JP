---
title: PidTagCorrelate の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ce8573310e17e26b4e2deb4c0a0f835a6569151e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802661"
---
# <a name="pidtagcorrelate-canonical-property"></a>PidTagCorrelate の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージの送信者のメッセージング システムの相互関係の機能を要求する場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CORRELATE  <br/> |
|識別子:  <br/> |0x0E0C  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>備考

元の送信メッセージと受信したレポートの相関関係を要求するこのプロパティを使用します。 トランスポート プロバイダーでは、true を指定する**PR_CORRELATE**のセットを使用して発信されたメッセージが検出されると、そのメッセージのメッセージ転送システム (MTS) 識別子を**PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) のプロパティを設定します。
  
 X.400 など、MTS の id では、メッセージの相関関係をサポートしているシステムで**PR_CORRELATE**を使用してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

