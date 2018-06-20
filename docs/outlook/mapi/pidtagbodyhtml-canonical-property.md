---
title: PidTagBodyHtml の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 19f0398d5e36cce13467a4fae86c4ea1d4019dd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802521"
---
# <a name="pidtagbodyhtml-canonical-property"></a>PidTagBodyHtml の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ハイパー テキスト マークアップ言語 (HTML) バージョン メッセージのテキストにはが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_BODY_HTML、PR_BODY_HTML_A、PR_BODY_HTML_W  <br/> |
|識別子:  <br/> |0x1013  <br/> |
|データを入力します。  <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティには、 **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)) が、html 形式では、同じメッセージ テキストが含まれています。 
  
HTML をサポートしているメッセージ ・ ストアは、その**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) で**STORE_HTML_OK**フラグを設定することによってこれを示します。 
  
 **メモ****STORE_HTML_OK**は、Microsoft® Exchange 2000 Server 以前のバージョンとが含まれている Mapidefs.h のバージョンでは定義されていません。 **STORE_HTML_OK**が定義されていない場合は、0x00010000 の値を使用してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

