---
title: PidTagAttachMimeSequence の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeSequence
api_type:
- HeaderDef
ms.assetid: d2a84f24-b4a5-4e16-9219-7a579a31a8f8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e46a6556b88452fb453b031fc1a90762fd748f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802508"
---
# <a name="pidtagattachmimesequence-canonical-property"></a>PidTagAttachMimeSequence の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
MIME メッセージの添付ファイルの MIME のシーケンス番号が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_MIME_SEQUENCE  <br/> |
|識別子:  <br/> |0x3710  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージの添付ファイルのプロパティ  <br/> |
   
## <a name="remarks"></a>備考

このプロパティが使用される MHTML をサポートするためです。 MIME メッセージの MIME のマルチパートのボディ部の親内の添付ファイルのシーケンス番号を表します。
  
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

