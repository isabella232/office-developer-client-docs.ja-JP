---
title: PidTagSubject の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 63bb5534756f44aebd9e6ca21c336534b279909d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803611"
---
# <a name="pidtagsubject-canonical-property"></a>PidTagSubject の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
全メッセージの件名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |あるの PR_SUBJECT、PR_SUBJECT_A、PR_SUBJECT_W  <br/> |
|識別子:  <br/> |0x0037  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、すべてのメッセージ オブジェクトに対して推奨されています。 
  
これらのプロパティは、常にフルの件名のテキストをプレフィックスと正規化された件名を連結したものでは、です。 プレフィックスがない場合は、正規化された件名は、件名の場合と同じにします。 メッセージを保存またはトランスポートのこれらのプロパティとルールを使用する正規化された件名を計算するために**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) のプロパティの両方は、 **PR_NORMALIZED_SUBJECT** ([で説明されているプロバイダーの使用PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))。
  
256 文字は、通常は短い文字列は、件名のプロパティと、メッセージ ストア プロバイダーがそれらに**IStream**インターフェイスをサポートする義務を負いません。 クライアントは、 **IMAPIProp**インターフェイスを介してアクセスを最初に試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ、 **IStream**に頼る必要があります常に。 
  
レポートの場合は、このプロパティは、元のメッセージの件名の前に、メッセージに何が起こったかを示す文字列を含みます。
  
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

