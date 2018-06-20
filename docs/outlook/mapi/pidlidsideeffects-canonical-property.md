---
title: PidLidSideEffects の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 479ba1990f7cac1768fc5e514e3fc55f017e4a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802161"
---
# <a name="pidlidsideeffects-canonical-property"></a>PidLidSideEffects の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ オブジェクトの処理方法によって、クライアント エンド ・ ユーザーの入力で動作している場合を制御します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidSideEffects  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008510  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>備考

ビットごとまたは 0 個以上の以下のフラグを設定する必要があります。
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |削除するときに、メッセージ オブジェクトの追加の処理が必要です。  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |UI は、メッセージ オブジェクトに関連付けられているではありません。  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |"IPF の**PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) のプロパティを使用してフォルダーのオブジェクトに移動またはコピーするときは、メッセージ オブジェクトに追加の処理が必要。"注意してください。  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |別のフォルダーにコピーするとき、メッセージ オブジェクトに追加の処理が必要です。  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |別のフォルダーに移動するときは、メッセージ オブジェクトの追加の処理が必要です。  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |エンド ・ ユーザーに動詞を表示する場合、メッセージ オブジェクトに追加の処理が必要です。  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |削除操作を元に戻すことはできません、"seOpenToDelete"が設定されていない限り、設定されていない必要があります。  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |コピー操作を元に戻すことはできません、"seOpenTocopy"が設定されていない限り、設定されていない必要があります。  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |移動操作を元に戻すことはできません、"seOpenToMove"が設定されていない限り、設定されていない必要があります。  <br/> |
|seHasScript  <br/> |0x2000  <br/> |メッセージ オブジェクトには、エンド ・ ユーザーのスクリプトが含まれています。  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |追加の処理は、メッセージ オブジェクトを完全に削除する必要があります。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

