---
title: PidTagRemoteProgress の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4e6495d5521e0f277ac4d501a987de0142d0960d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803316"
---
# <a name="pidtagremoteprogress-canonical-property"></a>PidTagRemoteProgress の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このプロパティには、リモート転送の状態を示す数値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_REMOTE_PROGRESS  <br/> |
|識別子:  <br/> |0x3E0B  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

転送が進行中でない場合は、このプロパティを 1 に設定する必要があります。 転送が進行中である場合、設定値を 0 ~ 100% の完了の転送のパーセントを示します。
  
数値ステータス コードに関連付けられているテキストは、 **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) のプロパティに表示されます。
  
このプロパティには、次のフラグを設定できます。
  
MSGSTATUS_REMOTE_DELETE
  
> メッセージ転送が削除されます。
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> メッセージの転送は実行中です。
    
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
