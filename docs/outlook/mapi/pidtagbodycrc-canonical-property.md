---
title: PidTagBodyCrc の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802529"
---
# <a name="pidtagbodycrc-canonical-property"></a>PidTagBodyCrc の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ テキストの巡回冗長検査 (CRC) の値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_BODY_CRC  <br/> |
|識別子:  <br/> |0x0E1C  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>備考

メッセージ ・ ストアには、PT_LONG の値を生成する任意の CRC アルゴリズムを使用できます。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの一部としてこのプロパティを計算すると、最初に、後で変更されるたびに ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティが設定されていること必要があります。
  
**PR_BODY**プロパティまたはその変種に含まれるメッセージのテキスト文字列を比較するを支援するクライアント アプリケーションが**PR_BODY_CRC**を使用します。 このプロパティを使用するクライアント迅速かつ容易に検出できるメッセージのテキストが変更されたとき。 **PR_BODY_CRC**を使用して**PR_BODY**をメッセージ ・ ストアから取得し、ローカル バージョンと比較することではなく、その大幅なパフォーマンス向上を実感できます。 
  
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

