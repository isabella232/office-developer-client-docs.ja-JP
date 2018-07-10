---
title: PidTagOriginCheck の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803122"
---
# <a name="pidtagorigincheck-canonical-property"></a>PidTagOriginCheck の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
配信レポートの受信者を元のメッセージの発生元を検証するを有効にするバイナリの検証値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ORIGIN_CHECK  <br/> |
|識別子:  <br/> |0x0027  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、送信されたメッセージの送信元を確認するメッセージ転送エージェント (MTA) または配信レポートを受信するメッセージングのユーザーなどのサード パーティ製の手段を提供します。 受信したメッセージに存在する場合、このプロパティは、メッセージへの応答として生成されるすべての配信レポートをコピーしてください。
  
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
