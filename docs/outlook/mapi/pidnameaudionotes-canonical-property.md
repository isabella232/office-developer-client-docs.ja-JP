---
title: PidNameAudioNotes の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAudioNotes
api_type:
- COM
ms.assetid: aec4d328-c192-4672-a478-b08442352794
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2eb1f0a517b430f2c96161e94faa22ec4d67ac41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802325"
---
# <a name="pidnameaudionotes-canonical-property"></a>PidNameAudioNotes の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ボイス メッセージに関連付けられている注釈テキストを指定します。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |UMAudioNotes  <br/> |
|プロパティを設定します。  <br/> |PSETID_UnifiedMessaging  <br/> |
|プロパティ名:  <br/> |UMAudioNotes  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |ユニファイド メッセージング  <br/> |
   
## <a name="remarks"></a>備考

閲覧、ボイス メッセージに直接オーディオ ノートを編集して、エンド ・ ユーザーを有効にするには、クライアントには、音声メッセージのオブジェクトのこのプロパティに追加されるメモのセットをユーザーが入力できる編集ボックスが用意されています。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> プロパティとは、ボイス メールと fax メッセージを表示するための許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
