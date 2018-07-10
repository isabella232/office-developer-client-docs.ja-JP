---
title: PidLidToDoTitle の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 66208b2d31ca379389f3249abf281dd4d040e276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802256"
---
# <a name="pidlidtodotitle-canonical-property"></a>PidLidToDoTitle の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
統合の to do リストでは、このメッセージ オブジェクトを識別するユーザーを指定できるテキストが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidToDoTitle  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085A4  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

タスクでこのプロパティを設定しない必要があります。 空のプロパティを指定するには、長さ 0 の文字列にこのプロパティを設定しないでが代わりにそれを削除します。 
  
メッセージ オブジェクト、およびプロパティのフラグを付けることが存在しない場合、クライアントは、このプロパティに**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) の値を記述する必要があります。
  
統合の to do リストでこのプロパティが存在しない場合、クライアント置き換える必要があります**PR_NORMALIZED_SUBJECT**プロパティの値を to do リストにこのプロパティを表示するときです。 
  
下書きメッセージ オブジェクトでは、[クライアントは、送信者のフラグを実装している場合このプロパティは、 **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) と同じ値に設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidTagNormalizedSubject の標準的なプロパティ](pidtagnormalizedsubject-canonical-property.md)
  
[PidLidFlagRequest ���K���̃v���p�e�B](pidlidflagrequest-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
