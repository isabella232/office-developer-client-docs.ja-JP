---
title: PidNameKeywords の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameKeywords
api_type:
- COM
ms.assetid: bcc0cda0-02bc-49a5-9fb9-850b4c2867c1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b71579a4652df62e696cd0dc6113dde44fad4287
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802338"
---
# <a name="pidnamekeywords-canonical-property"></a>PidNameKeywords の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
キーワードやメッセージのオブジェクトのカテゴリが含まれています。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |なし  <br/> |
|プロパティを設定します。  <br/> |PS_PUBLIC_STRINGS  <br/> |
|プロパティ名:  <br/> |キーワード  <br/> |
|データを入力します。  <br/> |PT_MV_UNICODE  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

メッセージのオブジェクトでは、このプロパティの複数値文字列内の各文字列の長さのカテゴリを指定する複数行文字列値は 256 未満である必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXODOC]](http://msdn.microsoft.com/library/103007c8-5066-4bed-84e3-4465907af098%28Office.15%29.aspx)
  
> プロパティは、ドキュメントに対する許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

