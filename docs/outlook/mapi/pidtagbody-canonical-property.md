---
title: PidTagBody の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 23d943d5576f5e9d7694b03c90dea79a878dee64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802511"
---
# <a name="pidtagbody-canonical-property"></a>PidTagBody の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ テキストが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_BODY、PR_BODY_A、PR_BODY_W  <br/> |
|識別子:  <br/> |0x1000  <br/> |
|データを入力します。  <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは通常、個人間メッセージ (IPM) でのみ使用されます。 
  
リッチ テキスト形式 (RTF) をサポートしているメッセージ ・ ストアは、メッセージのテキスト内の空白への変更を無視します。 **PR_BODY**が最初に保存されると、メッセージ ・ ストアも生成し、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティ、RTF 形式のメッセージ テキストを格納します。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出された後で、 **PR_BODY**が変更された場合は、メッセージ ・ ストアは、rtf 形式のバージョンとの同期を確実に[行う](rtfsync.md)関数を呼び出します。 プロパティを左の空白が変更されているだけの場合そのままです。 これには、任意の複雑な RTF メッセージが RTF に対応していないクライアントを通過するときの書式を設定して、メッセージング システムが保持されます。 
  
MAPI がで実行されているオペレーティング システムのコード ページでは、このプロパティの値を表す必要があります。 
  
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



[PidTagRtfInSync の標準的なプロパティ](pidtagrtfinsync-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

